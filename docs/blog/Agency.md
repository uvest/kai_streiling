---
title: Agency
---

# Agency

Feeling Agency (FoA) connects us to the world around us. It is often described as "the feeling of being in control, of being the source of ones thoughts, actions and their consequences." And equivalent to many feelings, we mostly don't notice Agency when we think, move or interact.

One well-known model about the source of this feeling of being in control is the comparator-model. This model works on the assumption that we constantly make predictions about our body and our world around us. Especially when we act, we feed a copy of the efferece signal (which we send to our muscles to move them) into a feed-forward model in our brain. This feed-forward model then predicts not only the outcome of this action, the resulting state, but also the corresponding sensory consequences: When I touch the hot oven, it will hurt. <br>
This predicted sensory consequence is then compared to what we actually sense. If they match, we feel Agency and everything goes as expected.

Additionally, sensing Agency over an outcome can be influenced by the action's context. It might be driven by our attention (where we look), our current environment (for example, if there are other people also doing things) and how much we (generally) believe to have an effect on the world around us.  Cue-integration models suggest that these cues, that is these pieces of information, are all combined into one experience of Agency.

## The Mario-Cart Effect
Think of the first time you played Mario Cart with some other people - potentially your friends. It might have happened that you thought you were performing pretty well. You might be a natural at this! <br>
Then you realised that while you were watching Luigi in the upper right corner leading the crowd, poor Yoshi in the bottom left was somehow running into a wall all the time. Wait. Didn't you choose Yoshi? <br>

If you need more anecdotal references, have a look at [these two playing an old pokemon game](https://www.youtube.com/shorts/L5hroU4SS3c){target=_blank} (Video in German, sorry). Hännö (Hand of Blood) and his friend show a perfect example of Confusion in their Sense of Agency. Or less scientifically, they are totally lost about which pokemon they control!

And there are two main drivers for this here:

1. Expectation matters. Given an action (button press) we expect an outcome. We make a prediction, using our internal model of the world. And if the result fits our prediction, we feel Agency about it.
 
2. Performance biases. We humans really do like to be good at what we are doing. And thus, we tend to rather attribute preferrable outcomes to our own actions: If it wins, it's me.

In our project, we simply went ahead and formalised this confusion in a Mario-Kart inspired, but somewhat simpler, game. We can detect from peoples behaviour, when they get confused - i.e. when they think they are Luigi instead of Yoshi - and test what makes them confused by varying the parameters of the game. For example, we can make the acting characters behave more similar to the player or we can vary how differently they look (Bowser, for example, might be easier to differentiate from Luigi than Yoshi (both are green) or Mario (both wear hats)). At the same time, we built a probabilistic model (some maths equations) that estimates based on people's actions (steering left or right) and the context of the game, which object they were most likely thinking to control.


