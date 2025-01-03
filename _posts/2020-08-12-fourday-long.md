---
title: Four Down Days and Long
hidden: true
date: 2020-08-12 07:23:45
---

Концепция этой стратегии состоит в том, чтобы открыть длинную позицию после того, как у основного рыночного индекса четыре дня подряд падают.
Теория состоит в том, что 4-дневный рыночный импульс для основных рыночных индексов трудно поддерживать, и что вскоре последует день роста.
Возможно, вам придется подождать день или два, пока он не появится,но в конце концов он появится. Эта реализация покупает на рынке,
открытом в 5-й день после 4-х дней падения.

---

# Код

```
using OpenQuant.API;

public class MyStrategy : Strategy
{
	[Parameter("Order quantity (number of contracts to trade)")]
	double Qty = 100;

	[Parameter("Number of consecutive down closes")]
	int ConsClosesCount = 4;

	int count;
	double prevClose;

	public override void OnStrategyStart()
	{
		prevClose = -1;
		count = 0;
	}

	public override void OnBar(Bar bar)
	{
		// we need at least one bar to go by before we do anything
		if (prevClose != -1)
		{
			// if we don't have a position open, increment the count of down days (or reset it to zero)
			if (!HasPosition)
			{
				if (prevClose > bar.Close)
					count++;
				else
					count = 0;

				// if this is the fourth (consClosesCount is equal to 4 by default) down day, 
				// issue a market order to open a long position tomorrow morning, on day 5
				if (count == ConsClosesCount)
					Buy(Qty, "Entry");
			}

			// else if we have a position open, close it now (today is the day after the trade was 
			// entered), so now is actually end of day 6, and the trade will be executed by the market 
			// on open day 7.
			else
				Sell(Qty, "Exit");
		}

		// today's close now becomes the previous close for the down day calculation
		prevClose = bar.Close;
	}
}

```
