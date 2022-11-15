# Recyclable-material-detection-model

Did you know that 40% of what goes into recycling bins cannot be recycled. This is because some people throw in items which are unsuitable for recycling.

#### Why is this a problem?

Contamination arises when wrong things are thrown into the blue recycling bin, such as food and liquids as well as items that cannot be recycled.

When this happens, this will contaminate the rest of the recyclables collected and waste the efforts of everyone.

Recyclables that are contaminated by food or liquids cannot be recycled which makes them no different from general waste. They will then have been disposed of, incinerated and landfilled.

That's why putting the right stuff in the right bin is important.

One proposed solution is to have artificial intelligence play a role by having it differentiate between recyclable and non recyclable items. With this, we will be able to pick out what should be thrown into the recyclable bins and what should be thrown into the garbage bins.

Using the yolov5 model by ultralytics, the model would be retrained with a dataset that identifies recyclable materials eg. glass. Paper, plastic, metal. The following pictures show the result of the model after training. The labels above show the A.I. 's guess as to what material the picture is showing and its confidence score beside it.

**Glass**
<img src="/results/recyclables detection 1"/>
<img src="results/recyclables detection 2"/>
<img src="results/recyclables detection 3"/>



**Paper**
<img src="results/recyclables detection 1"/>
<img src="results/recyclables detection 2"/>
<img src="results/recyclables detection 3"/>

![](RackMultipart20221115-1-6e8ko2_html_849501702f263c0b.png) ![](RackMultipart20221115-1-6e8ko2_html_5eefeda77e9840a7.png) ![](RackMultipart20221115-1-6e8ko2_html_3c85904586c0805b.png)

**Metal**
<img src="results/recyclables detection 1"/>
<img src="results/recyclables detection 2"/>
<img src="results/recyclables detection 3"/>



**Plastic**


As seen above, there are instances of metal cans being mistaken for glass and glass bottles being mistaken for plastic. There are multitudes of potential reasons why the A.I. behaves in this way.

In the case of the metal can being mistaken for glass could be that the metal can in the picture shown was not a type of metal can that was included in the training data. As the A.I. has not seen this type of metal can before, it characterises it towards the next most similar object, being glass.However, in the case of the glass bottle being mistaken for plastic, it could be that glass bottles and plastic bottles have a very similar look in terms of pixel patterns. In fact, if a picture of a glass bottle and a picture of a plastic bottle were given to a human to tell the difference based only off the picture, the human could also mix the two up. The reason why a human is able to tell the difference in the material is due to other factors such as thickness, rigidity or even the sound of the material when faced with an impact. In order to have the A.I. have a comparable efficiency to a human, these other inputs would have to be in play.
