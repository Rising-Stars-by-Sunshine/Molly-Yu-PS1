# # Title [How to Choice a Good Title?](https://www.nature.com/articles/s41562-021-01152-2)
## Project information
- **Author**: Molly Yu, Poliecon, 2023, Duke Kunshan University
- **Instructor**: Prof. Luyao Zhang, Duke Kunshan University
- **Disclaimer**: Submissions to the Problem Set No.1 for [COMPSCI/ECON 206 Computational Microeconomics, 2023 Spring (Seven Week - Second)](https://ce.pubpub.org/) instructed by Prof. Luyao Zhang at Duke Kunshan University.

## Table of Contents
- model
- code
- spotlight
- more about the author
- references

### Model
- Game Environment
Trust game, also called investment game, was created by Berg et al. (1995). It is a game from the experimental economics sector. The aim of the experiment is to study the trust and reciprocity in investment activities of society (Berg, Dickhaut, and McCabe 1995). The experiment is between two strangers. One receives an endowment at the beginning. The other receives the triple amount of money the previous one gives and gives back a random amount of money. The game is only one round (Miguel D, Maria E, and Mónica M 2017). The one who gives money first is seen as an allusion to investors and the one who receives and gives back are depositors. On average, among the 32 participants, investors gave 5.16 dollars out of 10 dollars and depositors returned 4.66 dollars round (Miguel D, Maria E, and Mónica M 2017). The result of the experiment claims to make economists think twice about the fundamental assumptions in market economy, the transaction happens because of the self-interest of people (Adam 2002), instead of the trust in strangers.
	The game described below is an edited version of the trust game. To better simulate the real investment that happens in society, I created a new game based on the trust game. There are still two players in the game. And the endowment for the investors is 100, and the money depositors receive is doubled. Instead of playing a one-shot game, the game goes for 2 rounds. Most importantly, to increase the impact of the amount of trust that players can have in the result of the game, I added a magnifier. A certain amount of money will be added or deducted from the investor’s account after each round the depositors give back the money. The amount of the money equals the money depositors send back (investment) minus the money investors give out (return). If depositors give more money than the investor sends out, then investors will be rewarded with the difference in the money and vice versa. This magnifier represents the opportunity cost that the money for investment and the return on the investment so that to emphasize the Matthew effect that happens in the finance world. 
	The payoffs of the two players are shown in the graph. 
![https://github.com/Rising-Stars-by-Sunshine/Molly-Yu-PS1/blob/main/table.png](image.jpg)
  Based on the calculated payoffs, there are different strategies for the two players. For investors, the profit depends on how much money is given back from the depositor each time. The problem for investors is to figure out what is the smallest number to give out to receive the biggest return from the depositor for each round. For depositors, the problem is what is the smallest number to give back in the first round to receive the biggest number in the second round. 

- Solution Concept
  Using backward induction, we start analyzing from the last step.
  For depositors, because they are the last ones to make the move, which is to give the money back, they can choose to betray the investors in the last round and well behave in the first round. In other words, they can give back more money in the first round to lure the investor to invest more in the first round and not give back in the second round.
  For investors, to receive more money at the end of the game, they have to increase the amount of money they receive and lower the initial investment. One way to figure out the right amount is to observe the investment return rate in the first round and decide how much money to give in the second round. For the first round, because there is no historical data, the investor can give their best guess of the investment rate and decide how much to invest in the first round. But after knowing the possible strategy for depositors, investors might invest less in the second round.

- Evaluations: e.g. efficiency and fairness
	Because there is no following game for both players, the depositors would care less about their reputation. Therefore, they will tend to betray in the last round, which is unfair to the investors. But if it is the real market, the investors and the depositors will have historical records for previous games before they start a new game. And this can greatly solve the fairness of the game for the depositors will try to have a good record, which is a good investment return rate, or they will gain nothing in the end. 
	The efficiency of the game is higher compared to the original trust game. Because there are two rounds in total. Both players will try to improve the efficiency in the first round by giving each other more money. 

### Code
How do I customize the demo?
I changed the endowment to 100, the multiplier to 2, the rounds to 2, and add a magnifier based on the difference between the investment and return. I also tell the players there is a magnifier effect on the introduction page, and remind the depositors t when they send money back using labels. 
Differences
The welfare of the two players in total will improve, because there are two rounds, and players can choose their next move based on the data from the last round.


### Spotlight
Behavioral experimental research paper: “Experiments based on Berg game about trust”

What research question does the behavioral experimental research intend to address? 
What is the relation between the amount sent by an investor and the initial capital available, and returned trust from an anonymous?

How does behavior in the experiments differ from backward induction? 
The investors increased the second investment based on the first round return, instead of decrease the investment because they know the other player can choose not to give the money back.

What is the behavioral (e.g., psychological, social) foundation that underpins the observed behavior?
People will predict others’ behavior using the previous decisions that others made. In this paper, the investors “learn” the return rate of the students from the first round, and expect that would be similar in the second round. 


### More about the Author
- headshot
![https://github.com/Rising-Stars-by-Sunshine/Molly-Yu-PS1/blob/main/spotlight/750_650%E5%A4%B4%E5%83%8F.png] (image.jpg)
- self-introduction
Senior at Duke Kunshan Univirsity, has an interest in econ, finance, behavior science. Now trying hard to learn CS.

### References

- Literature References in [Chicago Author-Date](https://www.chicagomanualofstyle.org/tools_citationguide/citation-guide-2.html) Style and [BibTex](https://scholar.google.com/) 

Levin, Dan, and Luyao Zhang. 2020. “Bridging Level-K to Nash Equilibrium.” *The Review of Economics and Statistics* 104 (6): 1329–40. https://doi.org/10.1162/rest_a_00990.
Adam, Smith. 2002. The Wealth of Nations. Oxford, England : Bibliomania.com Ltd.
Berg, Joyce E., John Dickhaut, and Kevin McCabe. 1995. “Trust, Reciprocity, and Social History.” Games and Economic Behavior 10 (1): 122–42. https://doi.org/10.1006/game.1995.1027.
Miguel D, Rojas, Valencia Maria E, and Diaz Mónica M. 2017. “Experiments Based on Berg Game about Trust.” Espacios 38 (March): 13. https://www.revistaespacios.com/a17v38n34/a17v38n34p13.pdf.

```
@article{levin2022bridging,
  title={Bridging level-k to nash equilibrium},
  author={Levin, Dan and Zhang, Luyao},
  journal={Review of Economics and Statistics},
  volume={104},
  number={6},
  pages={1329--1340},
  year={2022},
  publisher={MIT Press One Rogers Street, Cambridge, MA 02142-1209, USA journals-info~…}
}
```

