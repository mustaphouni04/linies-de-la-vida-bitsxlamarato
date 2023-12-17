# linies-de-la-vida-bitsxlamarato
## Inspiration
At the beginning of our project, our team drew on our combined knowledge in computer vision, making use of libraries like OpenCV. Recognizing the importance of working with images, we understood that this methods were essential for providing valuable insights throughout our project.

## What it does
Using SSIM (Structural Similarity Index Measure) on some samples drawn from some of the FCF (Fetal Heart Rate) that were given to us, we use templates of the Intrapartum fetal monitoring guide based on pathophysiology to recognize known patterns given a input sample.

We also use Corner Detection (Shi-Tomasi) on the FCF's given to us to find unknown patterns which may or may not be dangerous patterns (that is up to the medical professional which analyzes if it's unusual). That way we can design new patterns and make it helpful for professionals to use.

## How we built it
We used a series of libraries but the one we used the most was OpenCV (since we're dealing with images). We loaded the pdf's and got the images out of them. Then, we computed corner detection on the FCF of some pages to display the performance of the detection. We've used cv2.goodFeaturesToTrack to compute the corners and a threshold of 150 to get high quality corners but without losing some important details. Afterwards, we loaded all template images found in the Intrapartum fetal monitoring guide based on pathophysiology and we computed SSIM on sample and template to find similarities using only the ones that give the highest score. After that we set a threshold for the score of about 0.7 and generate an alert of what may or may not be a dangerous pattern.

## Challenges we ran into
We had some trouble while detecting corners: there was noisy and unwanted features which were still tracked and the algorithm found them to be of high quality or the maternal heart rate got in the way and those corners were also detected. Dealing with some images was tricky and we had to work on different color spaces and different kinds of threshold to properly separate the background from the FCF.

## Accomplishments that we're proud of
We're proud of having completed what we wanted which was to create a digital tool that involves pattern detection and an alert system that overall gives good results.

## What we learned
We extended our knowledge on Computer Vision techniques and some other methods to evaluate the precision on similarities in images.

## What's next for linies-de-la-vida-amb-IA | bitsxlamarató
More Hackatons!
