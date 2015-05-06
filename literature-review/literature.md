# Diabetic retinopathy kaggle challenge

## Literature review

DR can be characterised through the detection of abnormalities in fundus images:

* microaneurysms,
* cotton wool spots,
* exudates,
* macular edema,
* hemorrhages.

- [ ] Get "Visible manifestations of diabetic retinopathy", Phillips P.J.

From Sidibe et al. (2015), there is a common framework for these specific lesions detection:

* image quality specification,
* vessel segmentation,
* lesion detection,
* classification.

Giancardo et al. (2012) is an example of exudates detection.

Sidibe et al. (2015) proposed an interesting approach by first detecting which can of lesions can occur in the image, before to apply specific algorithm to quantify the DR stages.

- [ ] Check which lesions can be simutaneouly or not in the fundus image.

## Proposed ideas

It seems that we do not have anything else than the grading of the image in order to train. This the previous discussed method could be hard to apply since that you cannot learn specifically these lesions characterisitcs.

However, it should be possible to learn the grading characteristics. In all the cases, it should be really important to have a global normalisation accross all the images that they look alike as much as possible. However, it should exist some variability between the images belonging to different grades. It could be probably interesting to see if we can apply any normalisation but one that is in fact learning from the variation of the grading.

Once that every images is looking hopefully more less the same, I see the problem as learning a dictionnary for each grade since that the characterisitic should be different. However, bear in mind that the grade is the final output of the classifier and that learning different dictionnaries come back to not knowing how to combine them when applying them.

Another fact to consider is noise that can be added in the three components of the machine learning system. Noise in the samples, labels and feature dimensions. I think this is a great example where everything is noisy.

## Dataset specification

The dataset contains image with different artefacts:

* out of focus,
* underexposed,
* overexposed.

## Current projects

* https://github.com/hoytak/diabetic-retinopathy-code
