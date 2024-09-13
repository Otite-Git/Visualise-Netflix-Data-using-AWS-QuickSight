# 💻Visualise Netflix Data using AWS QuickSight☁️


Hi! Welcome to my repository containing my AWS Project I've have undertaken as an AWS expert and Cloud enthusiast⚡️:

In this repository you will see a description of the project, high level architecture, scripting files and information on other key assets that I have used to develop this project as part of my portfolio.


## **Project Overview** 

This project consists of using AWS QuickSight which helps in effectively analysing data and through creating visualisations. As part of this project, I will analyse a huge dataset of Netflix shows and movies to create a dashboard that extracts all the interesting insights

![High Level Architectural Diagram](https://github.com/user-attachments/assets/069c5e8e-177a-455a-8e26-817318a9dc8f)

- - - 
## **Architecture**

1. **Amazon S3:** Enables environmental file storage.
2. **Amazon Quicksight:** Enables users to visualise data, perform analysis, and share insights through interactive dashboards, reports, and charts.



## **Deployment Steps**
 ### Dataset Configuration
 1. The datasets which used for this project have been put together and can be found in the repository file section of this repository. They are titled ! [netflix_titles.csv](https://storage.googleapis.com/nextwork_course_resources/courses/aws/AWS%20Project%20People%20projects/Project%3A%20Visualise%20Data%20using%20Amazon%20QuickSight/netflix_titles.csv) and [manifest.json.](https://storage.googleapis.com/nextwork_course_resources/courses/aws/AWS%20Project%20People%20projects/Project%3A%20Visualise%20Data%20using%20Amazon%20QuickSight/manifest.json)

 ### Dataset storage in Amazon S3
 1. Open the S3 Console on AWS and select create Bucket.
 2. Name the bucket 'nextwork-quicksight-project-name' (replace with'name' your name).
 3. Region select would be depended on the region closet to the individual. On this basis, Select the region closest to you.
 4. Keep the rest of the setting as default and select 'create bucket'.
 5. Upload the CSV file and the 'manifest.json'file into the bucket.
 6. Copy the S3 URL of your ' netflix_titles.csv' file.
    ![Uploaded files and URI copied](https://github.com/user-attachments/assets/48726cf7-d96b-4fe2-922a-0a4254928152)
7. Open your 'manifest.json' file in your laptop's text editor - for example, TextEdit (Mac) or Notepad (Windows).
8. Replace the URI in the 'manifest.json' file with the S3 URI of your dataset. It is important to edit this file because the URIs needs to accurately reflect the object location.
9. Re-upload the edited 'manifest.json'file into your bucket, which you'll notice automatically replaces the existing one.

### Create your Amazon QuickSight account
1. Within the AWS Management Console, search and sigh up for Amazon QuickSight.
2. Sign up for a free trial of the 'Enterprise' edition if you don't have an account.
3. Make sure you uncheck this offer to upgrade box below:
   ![image](https://github.com/user-attachments/assets/38913750-26e9-47a3-8273-c231fd9f8e4c)
4. Enter your details for your QuickSight account ensuring the email used is the same email as your AWS account.
5. Select 'S3 Bucket' and select 'Select S3 Buckets'.
   ![image](https://github.com/user-attachments/assets/2d906461-4166-40c3-937f-715a3a5566f4)
6. Tick the box for the S3 bucket you created.
   ![image](https://github.com/user-attachments/assets/32eb29bc-5e04-4845-a9f1-26df20037483)
8. Select 'Create'to then ctreate the Amazon QuickSight account.


### Connecting the S3 bucket to Amazon QuickSight
1. From the left hand navigation bar, select 'Datasets'  then 'New dataset'.
2. Select 'S3'.
3. For the first field (source name), enter 'kaggle-netflix-data'.
4. Open a new tab to open your AWS Management Console again. Head back to your S3 bucket.
5. Select the checkbox next to 'manifest.json', then select 'Copy S3 URL'.
   ![image](https://github.com/user-attachments/assets/2330ed4f-5b33-4576-82d0-980d8390afb3)
6. Enter the S3 URL to your 'manifest.json'file and select connect.
   ![image](https://github.com/user-attachments/assets/5525c3b3-a27c-485b-ac42-a5e9ad3738b5)
7. Select 'Visualise'.
8. Select'Create'.
9. Select 'Interactive sheet' to start creating visualisations.

### Create Your QuickSight Visualisation
1. QuickSight, allows for sorting, filtering, and customisation of data top create visualisations. experimentation can also take place with different types of graphs like bar charts, pie charts, line graphs, etc.
2. On the left hand panel the dataset's fields are already imported.
   ![image](https://github.com/user-attachments/assets/2d60b34b-286e-495f-b0dc-981230b06108)
3. I have dragged 'release_year' into the Y-Axis heading to see a breakdown on the year that these Netflix-featured TV shows and movies were released.
   ![image](https://github.com/user-attachments/assets/32b38cd4-88fd-46c8-afce-37aae2e4e323)
4. Select the doughnut chart and resize it
   ![image](https://github.com/user-attachments/assets/12064c5b-4e21-432b-89c9-0d264a0063ff)
5. select '+ ADD' under the Visuals heading on your middle navigation bar, and you'll see another blank frame pop out.
6. Drag the 'release_year'label into the Y Axis heading.
7. Next, drag the 'type' label into the Group/Color heading.
   ![image](https://github.com/user-attachments/assets/87bad8fe-a24d-453c-9e9c-9e04a905f68f)
8. Here is an example of a data sheet created which reflects data on the different movie releases between specific time periods.
   ![Screenshot 2024-09-13 at 17 12 12](https://github.com/user-attachments/assets/0a2ff977-e185-4c9d-a808-691dc21a6bad)

### Adding titles to Visualisation
1. It is important for data to have titles that accurately reflect the information displayed. To add a title doouble click  titles of the charts you see in front of you.
2. The 'Edit Title' page will pop up. Enter the title to best describe the data which is being displayed.
   ![Screenshot 2024-09-13 at 17 22 55](https://github.com/user-attachments/assets/9ef2d3f2-2acf-4113-bcc9-788d044bf1fe)


### Publish a Dashbaord
1. Once the dashboard has been fully created, select 'Publish' on the right hand side. and give the dashbaord a name:
   ![Screenshot 2024-09-13 at 17 34 18](https://github.com/user-attachments/assets/38993186-e6ab-4ef9-a635-35e8595d5ff0)
2. Before clowint the QuickSight account and finishing this project, let's make sure to have a copy of the dashboard. On the top right hand corner, select the 'Export'icon.

    ![image](https://github.com/user-attachments/assets/546d9cc7-94f4-4017-82b9-9489fa83022b)
   
4. Select 'Generate PDFs' Wait for the PDF to be ready, then select 'Download' when you see that green banner pop up
   ![Screenshot 2024-09-13 at 17 48 53](https://github.com/user-attachments/assets/06837669-4fa6-4c21-8543-4b6d27e8760b)

### Clear and delete resources
1. returning to the home page, select the 'user' icon on the top right corner, and then 'Manage QuickSight'
2. Select 'Account Settings' from the left hand navigation panel, and then 'Manage' at the bottom of the page.
3. Toggle off account termination, and then type 'Confirm' before clicking'Delete Account'.

### delete the S3 bucket
1. Select your bucket, then choose 'Delete'.
2. You'll notice that you can't delete the bucket! There are still objects inside. Select'Empty Bucket'.
3. Type 'permanently delete'.
4. Once that's deleted, you should be able to delete the bucket itself.

## **Additional Resources**

- **AWS Documentation:** Refer to the [AWS documentation](https://aws.amazon.com/documentation/) for detailed guides on setting up S3 Bucket, IAM roles and Amazon QuickSight
- **GitHub Repository Files:** Refer to [Visualise-Netflix-Data-using-AWS-QuickSight](https://github.com/Otite-Git/Visualise-Netflix-Data-using-AWS-QuickSight/tree/main) to access the repository files for scripts, architectural diagrams, and configuration files necessary for this project.

## **Contributing**

Contributions to this project are welcome! Please fork the repository and submit a pull request with your enhancements


## **What problems did I solve by completing this project?**

1. **Simplicity:** 

## **What issues did I face while working on the project and how did I resolve that issue?**
  
- **Terraform Configuration Errors:** 

- **Terraform file setup Error:**
  
 ## **What overall lessons did I learn?**
 
- **AWS IAM (Identity and Access Management):** 

- **Terraform Basics:** 













