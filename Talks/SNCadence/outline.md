# LSST Cadence
- LSST covers the Southern Sky over 10 years in 6 bands. 
- Think of the survey in 2 parts: small area of many observations (Deep Drilling Field) and the Wide Fast Deep (WFD) with smaller number of observations with a median cadence of ~ 3 
- The cadence is actually quite non-uniform
- The observing strategy is under development, changes are possible and for SN science, we should be proactive in suggestions.


# How does this work?

- Currently we can study baseline cadences plus trial cadences produced by the Operation Simulator `OpSim`
- The Operations Simulator (OpSim) is an application that simulates the field selection and image acquisition process of the LSST over the 10-year life of the planned survey.
- In principle, you can run this, but the learning curve is steep, and it is changing, so this is not recommeneded at the moment. More generally, the instructions are [here](https://confluence.lsstcorp.org/display/SIM/How+to+Run+OpSim+and+MAF)
- __GOALS__ : Instead, we should (a) learn to study the OpSim outputs (b) Build metrics on them (c) Study simulations (d) Make requests for changes in OpSim outputs (ask Jeonghee Rho)


# OpSim Outputs : (Hands On from sqlite stack)
- Baseline Cadences: The project provides us with outputs of OpSim runs + postprocessing
- sqlite database: ~ 4 Gigabytes
- Multiple tables : Will list in a moment
- Important tables : Summary (~900 MB) , Proposal (super tiny), 
- Try examples to read OpSim outputs [in this notebook](Cadence_And_OpSim.ipynb)
- get schema (cmd line)

# OpSim output Description
- python pandas (to show quantities)
- OpSim output documentation explaining all columns [here](https://www.lsst.org/scientists/simulations/opsim/summary-table-column-descriptions-v335)
- sql queries from python
- sql queries on pandas

# Problems with getting to stated goals of doing simulations
- OpSim Outputs give us information on Pointings which overlap and dither. So a single SN could belong to many of these pointings. Very hard to do any meaningful calculation.
- Solution: Don't think in terms of pointings. Think in terms of (a) either single SN or (b) spatially neighboring sets of supernovae via tesselations 
- Different flavors of this solution are used in : MAF,  SNSims, SNANA

# MAF notebooks
- Writing a new metric
- MonteCarlo metrics
- Maybe concentrate on heuristics

# Simulations
- Save files to disc with ipix, obsHistID as database
- Can get pointings for all SN in that region
- Easy to parallelize (see toy example)
