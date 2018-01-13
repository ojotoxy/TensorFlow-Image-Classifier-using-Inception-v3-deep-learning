Firstly you need to intall the inception model and following files to train the new images using the google inception model
In the working folder you must have follwing files
python retrain.py \
  --bottleneck_dir=tf_files/bottlenecks \
  --how_many_training_steps=500 \
  --model_dir=inception \
  --summaries_dir=tf_files/training_summaries/basic \
  --output_graph=tf_files/retrained_graph.pb \
  --output_labels=tf_files/retrained_labels.txt \
  --image_dir=training_dataset
  
  In my github link I could have uploaded many of these files like training_dataset and since many files are above 50 MB so cannot be uploaded so i am giving you thr link to download required files and training images could be downloaded from here.
  git clone https://github.com/koflerm/tensorflow-image-classifier.git

To download the images from the internet there are many tools available like image bulk downloader and various scripts are available here and i am attaching the python files to fetch the images from url and download them. Please download image_downloading.py and keyword_selection.py which i am attaching in this repository. You can download these files and enter the keywords in the file keyword_selection.py and run image_downloading.py.

Run the file train.sh by opening the terminal in the directory where you can download all the files using the link git clone https://github.com/koflerm/tensorflow-image-classifier.git and create a folder training_images and download the images there using the above mentioned script. PLease create different categories there which would be shown during real time prediction with probability of each

Finally when the training is over please run the file python classify.py name of testing image.
