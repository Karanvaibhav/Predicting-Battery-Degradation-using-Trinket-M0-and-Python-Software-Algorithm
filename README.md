# Predicting-Battery-Degradation-using-Trinket-M0-and-Python-Software-Algorithm

What Is Battery Capacity?

A useful battery has predictable behavior; it can supply a constant amount of power, for a predictable amount of time, within a narrow voltage range. The ‘capacity’ or ‘C rating’ for batteries is probably the most useful parameter to express this.

Capacity describes how much total energy can be delivered by the fully charged battery, in a nominal usage pattern. For small batteries such as those found in portable electronics, it is usually expressed in units of milliamp-hours (mAh). Much of this article will analyze a lithium battery with a C rating of 1300mAh. 

Notice, though, that milliamp-hours are not units of energy. Energy is the product of voltage, current, and time; milliamp-hours represent only current and time. It is inferred that the measurement is relative to a constant voltage; the nominal voltage of the battery. A nominal usage pattern will allow the battery to deliver its full C rating.

A very important part of this pattern is the discharge rate (in amps). Different battery chemistries have different limits on this. A simple and reasonable assumption to begin with is that you will get the rated amount of energy from a lithium battery if you discharge it at about 1⁄2 of the C rating, or less. So, for example, with our lithium battery rated at 1300mAh, we can only expect to draw this much energy from the battery if we keep the current flow below 650 milliamps on average. If this guideline is followed, it will take two hours or more to fully discharge the battery.

As another example of discharge-rate limits, consider NiMH AA cells. Many manufacturers specify that the nominal discharge rate for NiMH cells is 1/5 of the C rating. 




Estimating Battery Age and Capacity:

It is common to describe battery age in terms of present capacity versus original (new) capacity, and that is what we will do here. We will continuously monitor the voltage and current at the high side of our battery while it is in use and discharging. This is the raw data on which we will apply our software algorithm.

First, we will estimate the present capacity of the battery. We can do this within the timeframe of one reasonably long discharge event. It doesn’t need to be a complete discharge event (more on this later).

Finally, the present capacity estimate can simply be compared to the manufacturer’s specified ‘new’ capacity, giving the user a percentage-degradation. 



 
