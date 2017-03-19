During my journey of studying Machine Learning I've been noting down thoughts I've had along the way.  There is a broad theme of trust in AI, which is an area of interest to me.

# Common-sense and side effects in AI Safety

The [Concrete problems in AI safety](https://arxiv.org/abs/1606.06565) paper  describes five key problems that need to be solved on the way to achieving safety of general AI. Some say the first of these, 'Avoiding Negative Side Effects', is the hardest, because we don't even have a clear definition of what a side effect is. The example given in the paper is of a cleaning robot knocking over a vase in order to clean faster.

It strikes me that humans actually have to learn what a side effect is too, and it comes from our model of the world and what we call 'common sense'.  For example, we know that vases are valuable, fragile and liable to fall over, so we try not to bump into them.  In this case what drives us perhaps is a general desire not to destroy value.  Or it could be the concept of ownership of objects, and that it is undesirable to pay the social and material cost of breaking someone else's vase.

Much of this could be formalised, and learnt, by crawling the web and mining it for relationships and arguments.  For example, you could learn that object 'vase' has attributes 'is valuable' and 'is fragile', and that being an object it probably has an owner. This knowledge could then be applied to a wide range of problems.

This proposal seems to be absent from the paper - if you know why or have something to add, I'd be very interested to hear!


# What you don't do online tells us something about you
We had a fascinating talk by Thore Graepel presenting his a paper he co-authored, [Inferring the Demographics of Search Users](https://www.gsb.stanford.edu/sites/gsb/files/conf-presentations/www2013.pdf), where Facebook users' demographic information was predicted fairly accurately from their Facebook 'likes'.

It raises the interesting question about what would be a strategy to keep a low-profile on Facebook.  At first you might think that you should just not 'like' anything, but that actually gives away a lot of information about you, particularly your attitude to Facebook and online privacy.

I've begun to see it a bit like wearing clothes for bodily privacy - wearing no clothes at all is not a good strategy for blending in!  Instead you perhaps need to wear average and inconspicuous clothes.

So returning to Facebook, perhaps the best way to keep a low profile would be to 'like' some very standard things, like football and fish & chips.  It would be interesting to figure out exactly what would be the most inconspicuous combination.

Another strategy could be to defy categorisation altogether, so whatever was inferred about you has very low precision.  For example, if you were to 'like' a completely random combination of topics you would still stand out, as you would if you wore random clothes, but it would be very hard to make confident inferences about you because nobody else has behaved similarly. This approach too would give away information about your attitude to online privacy...

# Human-human trust as an emergent property of our lack of acting abilities

If you have seen films like Ex Machina you may have wrestled with the question of how do you know if a robot is inherently trustworthy, or just advancing its own interests by merely pretending to be trustworthy.

So even if a robot does not betray your trust for ten years, you cannot know whether that is genuine.  It could have just been in its internal 'trustable' mode and could change at any time.

Most humans, by contrast, are not able to act convincingly in social situations over a long period of time. So if your neighbour is always friendly and dependable over a period of ten years with never a hint of anything else, it is probably genuine. He or she would never be able to act that way convincingly for so long.

So your ability to place trust them is aided by their inability to act convincingly over the long term.  In a sense, aspects of their personality are fully observable over the long term because they are unable to hide them well. It is fascinating to me that an individual limitation (inability to act convincingly) can give rise to useful higher-level concepts such as trust.

As we search for ways to design multi-agent systems of robots and algorithms that are trustworthy, perhaps we will need to place restrictions on them at an individual level that will enable properties such as trust to emerge.  Extending the analogy, perhaps we will need community- and society-level limitations in order to build this kind of property at a global level.

Contrast this with an example using autonomous cars.  When all cars are autonomous, what is to stop pedestrians crossing the road at any time?  The cars will all screech to a halt to avoid hitting the pedestrian.  This is, of course, a good thing, but could end up causing chaos on the roads if many people did it for fun.  One of the reasons we don't do this at the moment is that we can't fully depend on the drivers to notice us and stop in time.

So in this example it's our *lack* of trust in the abilities the other humans that helps prevent chaos on the roads.  Much further thought is needed, obviously, but it may be that we need to introduce small human-style imperfections in the autonomous car software in order to prevent mischevous pedestrian behaviour and so keep the traffic flowing.  Sharing the road is, after all, a social interaction.


# Why do we trust horses?
Horses can be thought of as learning agents.  They are controlled by a (real) neural network, and we have absolutely no idea how they work.  Yet when you ride them you trusting them with your safety.

I find it interesting to think about what it is that allows us to trust them.  Below are some thoughts, but actually there are many, many aspects to this and every person I have spoken to so far about this has had their own ideas too.

* Because they have been used by humans for so long, we have the sense that they are inherently trustable.  I guess you could say that they are known to be trustable in our collective human memory. This collective memory remains relevant because the horse population can only change its makeup slowly (generation to generation) - if all horses were suddenly 'reprogrammed' tomorrow we'd be back to square one in terms of trust.

* Horses tend to exhibit personalities, and personalities are passed down the generations to some extent, like in humans. Particularly docile horses are likely to produce particularly docile offspring.  So we have quite a lot of information about a horse's likely personality from its parents' record of behaviour.

* Horses exhibit emotions, like fear, nervousness etc., that we can relate to.  This strengthens our bond with the horse and essentially improves our own modelling of the horse. The horse can learn to trust us, too, and so cope better in stressful situations.  For example, if startled it might want to bolt, but may obey the rider's instruction not to because it senses the rider is calm.

There are lessons here for how we make trustable algorithms.  They may need to have periods when they do not update, or update slowly.  They may need to show something similar to emotions.  And they may need to model us as we interact with them, to learn how much they can trust our judgement when it contradicts their instincts.

# A car fleet as a distributed computing network
As we all know, cars contain more and more computing power, including GPUs, as they rapidly advance towards autonomy.  They are also becoming connected, with data flowing between the fleet of cars and the development centre. Even those cars that are not autonomous are starting to have sophisticated driver assistance systems.

Car companies need vast amounts of computing power to develop the autonomous driving algorithms and to train the models to analyse their data. So it begs the question of whether the GPUs on the cars themselves can be harnessed to do this.

After all, cars are not used 24/7, and many are now plugged in overnight to charge.  Even if they weren't plugged in, electric cars have such large batteries that you could run a GPU for some hours and not see an appreciable drop in charge.

What's better is that in some regions (e.g. northern Sweden) cars are plugged in overnight to power a small electric heater to stop the engine freezing solid and to heat the cabin slightly - presumably they do something similar with electric cars too. So in this case the owners are actually already paying for their car to turn electricity into heat.  So why not do it via its GPU instead of via its heater?

The numbers here could be quite significant.  When you consider that large car companies sell in excess of 10m cars per year, even if only a small fraction of them had GPUs that were available it would still be a very sizeable resource.

Of course, as a distributed computing platform it is not ideal, and would require algorithms that are able to run on an ever-changing number of processors and with potentially low-bandwidth communication, but it still could turn out to be useful for some applications.
