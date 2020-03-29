### Todos

- [ ] Update notebook, to use get_option_price
  - [ ] This way when we can redefine it to adjust
- [ ] Update notebook, to take advantage of Q Ratio
- [ ] Update notebook, to try a strategy like
  - 60/40 cash when Q ratio >1.25, all SPY < 1.25

### Essay outline

- Intro
  - Have been into Taleb and friends for a while. Has worked out with professional pursuits, but hadn't tried it with finance
  - With what's happening in the markets, I got interested in Spitznagel, who succesfully hedged against this
  - To explore this, kicked off a reddit thread, and worked together with two killers
  - This essay will go over the journey, the lessons learned, and some engineering reflections on python and pandas
- Spitznagel's Tail Risk Hedging Explained
  - If you reduce you downside risk, you have a huge advantage during downturns -- you can buy capital cheaply, and your compounding is dope
    - Some illustrattion
- How it's done, what is an option?
  - Explain options
- Giving this a try
  - Spitznagel's "Austrian Invesing I"
    - goal: 99.5% SPY, 0.5% puts, rolling every two months, adjusting based on Q Ratio
  - Get the data
  - Build the model
  - Write the strategy
  - Run backests:
    - Lessons learned
      - More OTM the better...buut the spread is very large in OTMs
      - If we can somehow get 80% of the ask price for ex, we do really well
    - Some more things
      - What if we did 60/40, alternating 
        - lessons
  - Some takeways
    - Engineering
      - Pandas has a _beautiful_ api -- python used in this setting gets as close to lisp as I've experienced in non-lisp languages
    - Finance
      - The tail risk hedging is indeed nuanced, and requires much more depth. Dealing with low volatility options is pretty unclear and hard
      - But, there's definitely something here.
        - I think Spitznagel's combo of risk hedging + value investing is something i want to get deeper on