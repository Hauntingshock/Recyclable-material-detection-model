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

![recyclablesdetection1](https://user-images.githubusercontent.com/113224356/201925141-168e17a4-d740-4bd0-86a9-afdf04f50220.PNG)
![recyclablesdetection2](https://user-images.githubusercontent.com/113224356/201925219-9ce7c648-d908-4451-ae6b-8b9eacbc3ea7.PNG)
![recyclablesdetection3](https://user-images.githubusercontent.com/113224356/201925227-ab5538f5-ce51-494e-8c26-a6b613fb5ec1.PNG)


**Paper**

![recyclablesdetection4](https://user-images.githubusercontent.com/113224356/201925375-0c2928a3-e6b8-4477-85ed-1c3a25d7822d.PNG)
![recyclablesdetection5](https://user-images.githubusercontent.com/113224356/201925383-6c81068c-c3f5-4b8f-88f5-2c0dcb67f0e0.PNG)
![recyclablesdetection6](https://user-images.githubusercontent.com/113224356/201925389-53c3386a-19fc-43f7-a212-aed748aedc18.PNG)


**Metal**

![recyclablesdetection7](https://user-images.githubusercontent.com/113224356/201925458-0913cbf1-0868-4f96-9552-855d2bbd066c.PNG)
![recyclablesdetection8](https://user-images.githubusercontent.com/113224356/201925461-3cda78f7-01f0-47e4-809d-50db1ceda23b.PNG)
![recyclablesdetection9](https://user-images.githubusercontent.com/113224356/201925466-03c191d8-6292-4f15-b623-fb47d8dd0677.PNG)


**Plastic**

![recyclablesdetection11](https://user-images.githubusercontent.com/113224356/201925519-5b44b1d3-c4c4-4eb1-b6c6-94ce4cc09ca9.PNG)
![recyclablesdetection10](https://user-images.githubusercontent.com/113224356/201925527-c0e692cd-03b9-49e0-899f-81f7659290a7.PNG)
![recyclablesdetection12](https://user-images.githubusercontent.com/113224356/201925528-40f8a144-f078-4f96-bfcd-4ca482b42c9e.PNG)



As seen above, there are instances of metal cans being mistaken for glass and glass bottles being mistaken for plastic. There are multitudes of potential reasons why the A.I. behaves in this way.

In the case of the metal can being mistaken for glass could be that the metal can in the picture shown was not a type of metal can that was included in the training data. As the A.I. has not seen this type of metal can before, it characterises it towards the next most similar object, being glass.

However, in the case of the glass bottle being mistaken for plastic, it could be that glass bottles and plastic bottles have a very similar look in terms of pixel patterns. In fact, if a picture of a glass bottle and a picture of a plastic bottle were given to a human to tell the difference based only off the picture, the human could also mix the two up. The reason why a human is able to tell the difference in the material is due to other factors such as thickness, rigidity or even the sound of the material when faced with an impact. In order to have the A.I. have a comparable efficiency to a human, these other inputs would have to be in play.

Finally in the case of the picture of multiple cardboard boxes not being detected, one could speculate that the reason the material was not detected could be due to the training data not having multiple cardboard boxes in such a compact area, thereby causing the model to group all of the cardboard boxes as one big material then determining that the pattern of pixels do not match the data that it has seen before.
