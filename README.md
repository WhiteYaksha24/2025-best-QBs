# 2025-best-QBs
Analyzing advanced stats of the 2025 season to discern a top 10 QB list

2025 NFL Quarterbacks: What Advanced Passing Stats Show

Which quarterbacks played best in the 2025 NFL season, and what do advanced passing stats reveal that standard stats don't?

Tools: SQL (SQLite) Data: Pro Football Reference, 2025 Advanced Passing

Scope and method
Included quarterbacks with at least 250 pass attempts (32 QBs).
Traded players appear on several rows. For Joe Flacco, I kept his combined 2TM row and removed his partial-season CIN row, which also passed the attempts cutoff.
Excluded non-QBs (punters, receivers, running backs) who threw a few passes.

Percentages like bad-throw rate and drop rate exclude spikes and throwaways.

A single season is a small sample, and some QBs missed many games, so differences between nearby players are not meaningful.

Question 1: When a pass doesn't connect, whose fault is it?

Compared each QB's bad-throw rate (Bad%) and drop rate (Drop%) to the league averages (15.7% and 4.3%).

Clean on both (9): including Joe Burrow, Geno Smith, Daniel Jones, Brock Purdy, Josh Allen, Drake Maye.

Struggles on both (10): including Bo Nix, Jared Goff, Patrick Mahomes, Matthew Stafford, Lamar Jackson, Caleb Williams.

Misses are on the QB (8): more bad throws than average, drops at or below average, including Baker Mayfield, Jalen Hurts, Aaron Rodgers, C.J. Stroud.

Receivers hurt him (5): drops above average, bad throws at or below, including Trevor Lawrence, Justin Herbert, Dak Prescott.

Standouts: Trevor Lawrence's drop rate (8.3%) was almost double the league average despite better-than-average accuracy. Spencer Rattler had the lowest bad-throw rate (11.0%), and Michael Penix the highest (24.0%).

Limit: bad-throw rate does not account for throw difficulty, so QBs who throw deep are likely penalized. QBs near the average (Mayfield, Dak Prescott, Jaxson Dart) can flip on hundredths of a point.

Question 2: Does holding the ball longer mean more pressure?

Split QBs at the league-average pocket time (PktTime).

Group, # of	QBs,	Avg pocket time,	Avg pressure rate

Quick release,	10,	2.26 sec,	20.0%

Slow release,	22,	2.44 sec,	22.1%

Slow-release QBs faced slightly more pressure, but the gap is small (about 2 points) and the groups are uneven.
Some QBs do break the pattern: Brock Purdy had the longest pocket time (2.7 sec) but only 21.1% pressure.
Pressure rate also depends heavily on the offensive line, so pocket time alone does not explain it.

Question 3: Does play action help, and who relies on it most?

Compared yards per attempt on play-action throws to yards per attempt overall, for the 25 QBs with at least 50 play-action attempts.

23 of 25 QBs gained yards on play action. The median gain was about 0.7 yards per attempt.
Largest gains: Lamar Jackson (+3.87), Kirk Cousins (+3.08), Sam Darnold (+2.85). Only Darnold's came on more than 100 throws (123).

Worse on play action: Aaron Rodgers (-1.11) and Patrick Mahomes (-0.55).

Heavy usage did not guarantee a bigger gain: Matthew Stafford used it on 34.7% of throws and gained +0.54.

Limits: samples are 57 to 207 throws per QB, and play action may reflect scheme and running game more than the QB.

Composite ranking: top 10 QBs

Ranked all 32 QBs on three measures, then averaged the ranks (lower is better):

Accuracy: bad-throw rate (lower is better)
Downfield production: completed air yards per attempt (higher is better)
Pressure faced: pressure rate (lower is better)

Rank, QB,	Team,	Games,	Accuracy rank,	Downfield rank,	Pressure rank,	Avg rank
1	Daniel Jones,	IND,	13,	4,	5,	11,	6.7

2	Spencer Rattler,	NOR,	9,	1,	17,	4,	7.3

3	Brock Purdy,	SFO,	9,	5,	5,	14,	8.0

4	Mac Jones,	SFO,	11,	9,	11,	5,	8.3

5	Sam Darnold,	SEA,	17,	11,	3,	13,	9.0

6	Drake Maye,	NE	,17,	8,	1,	19,	9.3

7	Josh Allen,	BUF,	17,	7,	17,	6,	10.0

8	Dak Prescott,	DAL,	17,	6,	9,	17,	10.7

9	Joe Burrow,	CIN,	8,	2,	16,	18,	12.0

10	Tyler Shough,	NOR,	11,	17,	11,	9,	12.3

Just outside the top 10: Trevor Lawrence and Matthew Stafford (tied, 12.7).

How to read this ranking

It measures only accuracy, downfield production, and pressure faced. It does not include touchdowns, turnovers, wins, or overall efficiency, so it is not a verdict on who was the best QB.

Several top-10 QBs missed many games (Rattler, Purdy, and Burrow played 8 to 9), so their rankings come from fewer plays.

Pressure rate mostly reflects the offensive line. With pressure removed and only accuracy and downfield production used, Daniel Jones and Drake Maye tied for first (4.5), Purdy moved to third, and Rattler and Mac Jones dropped out of the top five. The top group is closer than the order suggests.

Matthew Stafford, the 2025-26 MVP, ranks tied for 11th here because of his bad-throw rate (28th). The gap shows these measures miss things award voters weigh.
