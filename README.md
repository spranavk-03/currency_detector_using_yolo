<h1 align="center">Currency Detector using YOLO</h1>

<br>

<h2>Step 1: Gather Data</h2>

<ul>
  <li>Gather images of the objects you want the model to detect.</li>
  <li>In this case, we detect Indian currencies.</li>
  <li>For smaller datasets, take 30–40 images per object.</li>
  <li>Use images with different angles, lighting, and backgrounds.</li>
  <li>You can obtain datasets from https://www.kaggle.com/
  </li>
</ul>

<p align="center">
  <img src="./images/kaggle_currency.png" width="600"/>
</p>

<hr>

<h2>Step 2: Annotating</h2>

<ul>
  <li>Annotating means drawing a box around an object and assigning it a label.</li>
  <li>This helps the model understand what the object looks like and where it is.</li>
  <li>We will use Roboflow for annotation (free tool).</li>
</ul>

<h3>How to annotate:</h3>

<ol>
  <li>Open https://roboflow.com/ and create an account.</li>

  <li>
    Create a workspace, select public plan, and continue.
  </li>
</ol>

<p align="center">
  <img src="./images/RoboFlowLoginPage.png" width="600"/>
</p>

<ol start="3">
  <li>Create a project.</li>
</ol>

<p align="center">
  <img src="./images/RoboFlowProjectPage.png" width="600"/>
</p>

<ol start="4">
  <li>Fill in name, annotation group, select "Object Detection", and create project.</li>
</ol>

<p align="center">
  <img src="./images/RoboFlowClassificationPage.png" width="600"/>
</p>

<ol start="5">
  <li>Go to the "Upload Data" tab and upload your images.</li>
</ol>

<p align="center">
  <img src="./images/RoboFlowDataSetUploadPage.png" width="600"/>
</p>

<ol start="6">
  <li>Click on "Start Labelling" → "Assign to Myself".</li>
  <li>Draw bounding boxes around objects and label them.</li>
</ol>

<p align="center">
  <img src="./images/RoboFlowAnnotationPage.png" width="600"/>
</p>

<ol start="8">
  <li>After annotating all images, click "Add to Dataset".</li>
  <li>Preview your dataset.</li>
</ol>

<p align="center">
  <img src="./images/RoboFlowDataSetPage.png" width="600"/>
</p>

<ol start="10">
  <li>Split data into Train, Validation, and Test sets (recommended split is fine).</li>
</ol>

<p align="center">
  <img src="./images/RoboFlowTrainTestSplitPage.png" width="600"/>
</p>

<ol start="11">
  <li>
    Go to "Versions" tab and create a version.
    <ul>
      <li>Augmentation helps improve model robustness.</li>
    </ul>
  </li>
</ol>

<ol start="12">
  <li>Create the version.</li>
</ol>

<p align="center">
  <img src="./images/RoboFlowVersionPage.png" width="600"/>
</p>

<hr>

<h2>Step 3: Training the YOLO Model</h2>
