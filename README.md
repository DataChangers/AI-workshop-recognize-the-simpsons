# AI Workshop: Recognize The Simpsons
Create a model to recognize the main characters of The Simpsons
<!-- wp:heading {"level":1} -->
<h1>Build a model to recognize The Simpsons</h1>
<!-- /wp:heading -->

<!-- wp:paragraph -->
<p>Are you familiar with The Simpsons? Do you know the main characters? In case you don't, this workshop solves your problem! In this AI workshop you learn how to build a model to recognize the main characters of The Simpsons in 5 steps with an image dataset and Microsoft's <a rel="noreferrer noopener" aria-label="Custom Vision  (opens in a new tab)" href="https://www.customvision.ai/" target="_blank">Custom Vision </a>service. You need an Azure subscription to do so. If you don't have one, you can start a trial <a rel="noreferrer noopener" aria-label=" (opens in a new tab)" href="https://azure.microsoft.com/en-us/free/?WT.mc_id=AI-MVP-5002978" target="_blank">here</a>.</p>
<!-- /wp:paragraph -->

<!-- wp:heading -->
<h2>Step 1: Get The Data</h2>
<!-- /wp:heading -->

<!-- wp:paragraph -->
<p>The data for this workshop comes from Henk Boelman as part of the  <a rel="noreferrer noopener" aria-label=" Developers Guide to AI (opens in a new tab)" href="https://workshops.henkboelman.com/developers-guide-to-azure-ai/" target="_blank">Developers Guide to AI</a>, where you can find a link to <a rel="noreferrer noopener" aria-label="The Simpsons Lego dataset (opens in a new tab)" href="https://github.com/hnky/dataset-lego-figures/raw/master/_download/simpsons-lego-dataset.zip" target="_blank">The Simpsons Lego dataset</a>. Download this file and unzip it.</p>
<!-- /wp:paragraph -->

<!-- wp:heading -->
<h2>Step 2: Set Up The Environment</h2>
<!-- /wp:heading -->

<!-- wp:paragraph -->
<p>We are going the build the model to recognize a character of The Simpsons with Microsoft's Custom Vision service. Please go the the <a rel="noreferrer noopener" aria-label="Custom Vision website  (opens in a new tab)" href="https://www.customvision.ai/" target="_blank">Custom Vision website </a>and sign in. If you don't have a Microsoft account, you can create one <a href="https://signup.live.com/" target="_blank" rel="noreferrer noopener" aria-label="here (opens in a new tab)">here</a>.</p>
<!-- /wp:paragraph -->

<!-- wp:image {"id":15082} -->
<figure class="wp-block-image"><img src="https://www.datachangers.com/wp-content/uploads/2020/10/afbeelding-1024x643.png" alt="" class="wp-image-15082"/></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p><em> </em>Now create a new project:</p>
<!-- /wp:paragraph -->

<!-- wp:list -->
<ul><li>Give your project a name</li><li>Give your project a description</li><li>Select a resource. If you want to create a new you, simply click on "create new" and follow the steps (see screenshots below)</li><li>Select "Classification" as we want the model to put the images in different "classes", or characters of The Simpsons in our case</li><li>Select "Multiclass "Single tag per image"): we have images with only one character on it</li><li>Select "Retail (compact)"</li><li>Select "Basic platforms)</li></ul>
<!-- /wp:list -->

<!-- wp:paragraph -->
<p>Now click on "Create project" and your environment is ready to go!</p>
<!-- /wp:paragraph -->

<!-- wp:image {"id":15088} -->
<figure class="wp-block-image"><img src="https://www.datachangers.com/wp-content/uploads/2020/10/afbeelding-3-1024x611.png" alt="Recognize The Simpsons: create project" class="wp-image-15088"/></figure>
<!-- /wp:image -->

<!-- wp:image {"id":15087} -->
<figure class="wp-block-image"><img src="https://www.datachangers.com/wp-content/uploads/2020/10/afbeelding-2-1024x1019.png" alt="Recognize The Simpsons: create resource" class="wp-image-15087"/></figure>
<!-- /wp:image -->

<!-- wp:image {"id":15086} -->
<figure class="wp-block-image"><img src="https://www.datachangers.com/wp-content/uploads/2020/10/afbeelding-1-1024x516.png" alt="Recognize The Simpsons: create resource group" class="wp-image-15086"/></figure>
<!-- /wp:image -->

<!-- wp:heading -->
<h2>Step 3: Upload The Images</h2>
<!-- /wp:heading -->

<!-- wp:paragraph -->
<p>Now you are ready to upload the images, so you can train the model to recognize them. But we are not going to use all the pictures as we also want to test our model later on.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>First, click on "Add images"</p>
<!-- /wp:paragraph -->

<!-- wp:image {"id":15089} -->
<figure class="wp-block-image"><img src="https://www.datachangers.com/wp-content/uploads/2020/10/afbeelding-4-1024x618.png" alt="Recognize The Simpsons: Upload images" class="wp-image-15089"/></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>Go to the folder where you unzipped the images to. We start with Bart Simpson. In order to train the model, we have to inform the model what Bart Simpsons look like. Therefore, select part of the Bart Simpson images and give it a tag (name).</p>
<!-- /wp:paragraph -->

<!-- wp:image {"id":15090} -->
<figure class="wp-block-image"><img src="https://www.datachangers.com/wp-content/uploads/2020/10/afbeelding-5-1024x737.png" alt="Recognize The Simpsons: upload Bart Simpson" class="wp-image-15090"/></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>Give the images the tag "Bart Simpson" so the model can learn how to identify images of Bart Simpson.</p>
<!-- /wp:paragraph -->

<!-- wp:image {"id":15091} -->
<figure class="wp-block-image"><img src="https://www.datachangers.com/wp-content/uploads/2020/10/afbeelding-6-916x1024.png" alt="Recognize The Simpsons: Tag Bart Simpson" class="wp-image-15091"/></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>Please repeat this for the other characters of The Simpsons as well. You can click on "Add images" from the top menu to add more images.</p>
<!-- /wp:paragraph -->

<!-- wp:image {"id":15092} -->
<figure class="wp-block-image"><img src="https://www.datachangers.com/wp-content/uploads/2020/10/afbeelding-7-1024x608.png" alt="Recognize The Simpsons: add other characters" class="wp-image-15092"/></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>Now you have done your preparation and you are ready to train the model to recognize The Simpsons. Note: of course the model will only recognize the characters you entered...so there is room for improvement and you can add more characters to make the model more complete.</p>
<!-- /wp:paragraph -->

<!-- wp:heading -->
<h2>Step 4: Train The Model To Recognize The Simpsons</h2>
<!-- /wp:heading -->

<!-- wp:paragraph -->
<p>In order to train the model, start with clicking on the green "Train" button.</p>
<!-- /wp:paragraph -->

<!-- wp:image {"id":15094} -->
<figure class="wp-block-image"><img src="https://www.datachangers.com/wp-content/uploads/2020/10/afbeelding-8-1024x610.png" alt="Recognize The Simpsons: train the model" class="wp-image-15094"/></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>In this case, we go for a quick training.</p>
<!-- /wp:paragraph -->

<!-- wp:image {"id":15095} -->
<figure class="wp-block-image"><img src="https://www.datachangers.com/wp-content/uploads/2020/10/afbeelding-9.png" alt="Recognize The Simpsons: quick training" class="wp-image-15095"/></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>This will give you a trained model with some key performance indicators like Precision and Recall. We did pretty well :)</p>
<!-- /wp:paragraph -->

<!-- wp:image {"id":15096} -->
<figure class="wp-block-image"><img src="https://www.datachangers.com/wp-content/uploads/2020/10/afbeelding-10-1024x614.png" alt="Recognize The Simpsons: model performance" class="wp-image-15096"/></figure>
<!-- /wp:image -->

<!-- wp:heading -->
<h2>Step 5: Test The Model...Can Your Model Recognize The Simpsons?</h2>
<!-- /wp:heading -->

<!-- wp:paragraph -->
<p>Now it's time to test your model and run a quick test. Click on the "Quick Test" button.</p>
<!-- /wp:paragraph -->

<!-- wp:image {"id":15098} -->
<figure class="wp-block-image"><img src="https://www.datachangers.com/wp-content/uploads/2020/10/afbeelding-12-1024x614.png" alt="Recognize The Simpsons: quick test" class="wp-image-15098"/></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>This will open a popup to run the test.</p>
<!-- /wp:paragraph -->

<!-- wp:image {"id":15099} -->
<figure class="wp-block-image"><img src="https://www.datachangers.com/wp-content/uploads/2020/10/afbeelding-13-1024x616.png" alt="Recognize The Simpsons: test an unused image" class="wp-image-15099"/></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>You can browse for an <strong>unused</strong> image. Let's have a look...and yes! We got it right!</p>
<!-- /wp:paragraph -->

<!-- wp:image {"id":15100} -->
<figure class="wp-block-image"><img src="https://www.datachangers.com/wp-content/uploads/2020/10/afbeelding-14-1024x620.png" alt="Recognize The Simpsons: the result!" class="wp-image-15100"/></figure>
<!-- /wp:image -->

<!-- wp:heading -->
<h2>Further exploring AI</h2>
<!-- /wp:heading -->

<!-- wp:paragraph -->
<p>This workshop is part of the <a rel="noreferrer noopener" aria-label="Global AI Community October sessions (opens in a new tab)" href="https://globalai.live/october-sessions-getting-started/" target="_blank">Global AI Community October sessions</a>. </p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Of course there is much more to explore. Make sure you sign up for the <a href="https://globalai.community/" target="_blank" rel="noreferrer noopener" aria-label="Global AI Community (opens in a new tab)">Global AI Community</a> so you stay up to date.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Want to explore more? Then there are the workshops from Henk Boelman. bundled as the  <a rel="noreferrer noopener" href="https://workshops.henkboelman.com/developers-guide-to-azure-ai/" target="_blank">Developers Guide to AI</a>, or other exercises, like:</p>
<!-- /wp:paragraph -->

<!-- wp:list -->
<ul><li><a rel="noreferrer noopener" aria-label="AI Workshop: Predict Student Performance (opens in a new tab)" href="https://www.datachangers.com/ai-workshop-predict-student-performance/" target="_blank">AI Workshop: Predict Student Performance</a></li><li><a rel="noreferrer noopener" aria-label="AI Workshop: Predict Bike Demand (opens in a new tab)" href="https://www.datachangers.com/ai-workshop-predict-bike-demand/" target="_blank">AI Workshop: Predict Bike Demand</a></li><li><a rel="noreferrer noopener" aria-label=" (opens in a new tab)" href=" https://docs.microsoft.com/en-us/azure/cognitive-services/custom-vision-service/getting-started-build-a-classifier?WT.mc_id=AI-MVP-5002978" target="_blank">Build a fruit classifier</a></li><li><a rel="noreferrer noopener" aria-label="Build an object detector (opens in a new tab)" href="https://docs.microsoft.com/en-us/azure/cognitive-services/custom-vision-service/get-started-build-detector?WT.mc_id=AI-MVP-5002978" target="_blank">Build an object detector</a></li></ul>
<!-- /wp:list -->