# Digichem-Project-SEM-image-Processing
This is a Imperial Chemistry Department Digital Chemistry MSc Project. Contained is my code and resource.
The workflow is as follows: The collected images are grouped into labeled SEMs, unlabeled SEMs, and Museum Artworks for pertaining. 
The folders are processed with 1.Image Preprocessing.ipynb. The images are resized and their greyscales normalized. A reference folder is used, and the average greyscale CDF is calculated by that folder. This should be the labeled SEMs. The other folders are modified with respect to the greyscale of that image folder. 
In folder Preprocessed Images are all images already preprocessed, and can be used directly. 
2.and 3. are AE/VAE models, pretrain/finetuned on the three folders. The zip files of the three pre-processed images folders can be found in folder Preprocessed Images. 
After the AEs/VAEs are trained, 4./5. are used to extract AEs and VAEs features alongside appended Magpie features. They require correct correspondence between Template.csv and the labeled SEM images. The extracted features are stored in folder Extracted Features. In the folder, are all already extracted features, categorized into No Magpie, Full Magpie and Part Magpie. 
The extracted features can be passed to 6.supervised training.ipynb directly, and should show loss by epochs.
