## Transmission impairment

### Attenuation (Loss of signal)
When a signal travels through a medium it loses energy overcoming the resistance of the medium
Amplifiers are used to compensate for this loss of energy by amplifying the signal.

### Distortion (Change in signal shape)
Distortion occurs in `composite` signals.
Each frequency component has its own propagation speed  -> don't arrive at the same time so some parts of the signal have a phase shift.

### Noise
- thermal = `electrons make noise by moving more heat more moving`
- Induced = `From spools (induction) that are active in the system`
- Crosstalk  = `From signals through wires` 
- Impulse  = `Voltage spikes in powerplanes (Lightning, power lines)`

## Data Rate

### Nyquist Theorem
Nyquist gives the upper bound for the bit rate of a transmission for a noiseless channel

```math
C = 2*\text{Bandwidth}*\log_2(2n)
```

### Shannon’s Theorem
Shannon’s theorem gives the capacity of a system in the presence of noise.

```math
C = \text{Bandwidth} * \log_2(1 + \text{SNR})
```

## Performance

- Bandwidth = `(Frames per minute * frame size)/60`

- Propagation Delay = `Distance/Propagation speed`

- Transmission Delay = `Message size/bandwidth bps`

- Latency = `Propagation delay + Transmission delay + Queueing time + Processing time`
