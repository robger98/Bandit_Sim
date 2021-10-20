# Bandit_Sim

### Authors

Robert Geraghty

A python based multi-armed bandit simulator for CS5313/7313.


## About

This simulator generates an n armed bandit, with each arm having a normally distributed payout with a mean of (i+1)/(n+1) 
where i is the index of the arm and n is the number of arms for the band, and a common standard deviation that is passed as a parameter.

## Requirements

This code makes use of `Matplotlib` and `Numpy`

## Usage

First, to initialize a simulator you must:

```python
bandsim = Bandit_Sim(n_arms, payout_std, seed=seed)
```
If you want to veiw the histogram of all the arms, use the `plot` method to display two plots. This is done by:
```python
bandsim.plot(num_samples)
```
Where `num_samples` is the number of samples generated for each arm. The first plot generated shows the histogram of the data for each arm combined into one joint histogram.
The second plot shows multiple histograms, one for each arm of the bandit. This method can be useful to get a sense of the bandit problem.

To actually pull an arm of the bandit, you use:
```python
bandsim.pull_arm(n)
```
where `n` is the index of the arm you want to pull.

Finally, the arm means can be accessed with:
```python
bandsim.arm_means
```

## Support

If you find a bug please email me at rrg@utulsa.edu.
