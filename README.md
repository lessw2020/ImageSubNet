# ImageSubNet
Subsets of ImageNet, with corrected labelling and train/val balancing for accurate benchmarking 

## Improving benchmarking for optimizers and models with better data
While results on ImageNet are the current 'gold standard' that we all expect to see for any new model or optimizer for deep learning classifiers, there are multiple shortcomings inherent to Imagenet atm.
These include:</br>
1 - Cost to train against - ImageNet is 1.2M images, and on a single GPU, training can easily take a week and $100+ dollars.  For one test...</br>
2 - Images are in raw size rather than pre-sized - while this allows one to train very specific image sizes, it also means lots of additional compete redundantly done over and over every epoch. </br>
3 - Labels on some images are flat out wrong....for a gold standard benchmark, one wants to ensure the accuracy of ground truth or the measures taken from it are susceptible to randomness.</br>
4 - The balance of training images to validation images is often poor:  For some categories, you can have 1300 images with only 50 validation images, or < 4% validation size. That is a poor balance for using as a benchmark tool since the validation set is so small. 

Thus, the idea here is to correct some of the above shortcomings with a general ImageSubNet50 that includes a range of subgroups to expose both coarse and fine categorization, that would largely reflect a model or optimizers true capabilities at faster time to test, and more accurate testing.

To start, the first subset will be ImageBirds, which contains the following classes from ImageNet, and then will be rolled into the larger ImageSubNet50. 
n01614925 bald eagle </br>
![eagle_landing](https://user-images.githubusercontent.com/46302957/115128712-71e8f200-9f94-11eb-9ec3-955e63ba88f0.jpg)</br>
n01616318 vulture</br>
n01622779 grey owl </br> 
n01806143 peacock</br>
n01833805 hummingbird</br>

To show an easy example of some of the mis-labelling present in ImageNet
...in the bald eagle category of ImageNet we have this image of a vulture, which is a seperate ImageNet category.  This been removed for ImageBirds to ensure a more accurate dataset:
![vulture](https://user-images.githubusercontent.com/46302957/115128752-e885ef80-9f94-11eb-808e-3898387cd6e2.JPG)






