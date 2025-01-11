## Digital signals

Digital signals are being represented by multiple analog sine waves

![image-20250111140759193](Images/README/image-20250111140759193.png)

### Bandwith of a dedicated medium 

the Bandwidth of a medium acts like a band-pass filter letting on certain frequencies through. this means that our perfect digital signal that consist of infitante sine waves is now only letting throught the sine wave that are located in the bandwidth/bandpass-filter. 

![image-20250111140734380](Images/README/image-20250111140734380.png)

###  worst case scenario 

in the worst case scenario your medium only lets you send one sine wave without any harmonics. this can be described as: 
```math
\text{Frequency} = \text{Data Rate} / 2
```

![image-20250111140659984](Images/README/image-20250111140659984.png)

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

# Megan fox netwerk

# hamming code



