## :rocket: PORTFOLIO PIPELINE CREATION
This is basic of devOps using a personal portfolio to create a pipeline to deploy portfolio file to aws S3 Bucket using circleci automation tool


#### Prerequisites
1. Create [AWS Account](https://aws.amazon.com/)
2. Create [CIRCLECI Account](https://circleci.com/signup/) 

### ⚙️ Steps 
1. AWS 
  - S3 bucket set-up and deploy static files {HTML, CSS and all} with public access URl
  - IAM policy [check here](https://github.com/dev-luqman/DevOps_Room/blob/main/Portfolio/iam-policy.json)
![](./README_Docs/S3_deployment.jpeg)

```  ----  ```  ``` --- ``` ``` ---  ``` ``` --- ```

![](./README_Docs/s3_IAM.png)
  
```  ----  ```  ``` --- ``` ``` ---  ``` ``` --- ```
```  ----  ```  ``` --- ``` ``` ---  ``` ``` --- ```
```  ----  ```  ``` --- ``` ``` ---  ``` ``` --- ```

2. CircleCI Basic Commands
3. Basic Linus Command
4. Integrating and deploying from github to s3-bucket through circleci

### :book: AWS S3 bucket setup and static website deployment
Please follow the below steps to deploy your static website to s3 bucket

1. Login to [AWS](https://aws.amazon.com/) with your login details
![](./README_Docs/login.png)

``` --- ```   ``` --- ```   ``` --- ```   ``` --- ```

2. Search for S3 bucket in the search box
![](./README_Docs/search_s3_bucket.png)

``` --- ```   ``` --- ```   ``` --- ```   ``` --- ```

3. Create S3 bucket
![](./README_Docs/create_bucket.png)

  - Enter a unique name for your bucket
  - Enable ACLs 
![](./README_Docs/create_bucket_1.png)

  - Allow Block Access to your bucket 
  - Aknowledge the term to public access
  - Leave remaining as default and Click Create
![](./README_Docs/create_bucket_2.png)
![](./README_Docs/success_bucket_creation.png)

``` --- ```   ``` --- ```   ``` --- ```   ``` --- ```

4. Upload files to New_Bucket
  - Enter your Bucket by clicking on it
  - Upload your file/portfolio from your system [sample File here](https://github.com/dev-luqman/DevOps_Room/tree/main/Portfolio/page)
![](./README_Docs/open_bucket.png)
![](./README_Docs/uplaod_file_1.png)
![](./README_Docs/uplaod_file_2.png)
![](./README_Docs/uplaod_file_3.png)


``` --- ```   ``` --- ```   ``` --- ```   ``` --- ```

5. Enable Public access to files
  - Visit object tab under the bucket created
  - select all files
  - click on action and select ``` Make public using ACL ```
  - Under ``` Make Public ``` page, click Make Public
![](./README_Docs/enable_public_access_2.png)
![](./README_Docs/enable_public_access_3.png)
``` --- ```   ``` --- ```   ``` --- ```   ``` --- ```
  - Still goin on, CLick On ``` Property ``` Tab, 
  - Scroll down to Static website hosting ``` Edit ``` Tab
  ![](./README_Docs/edit_websit_hosting.png)

``` --- ```   ``` --- ```   ``` --- ```   ``` --- ```
  - CLick on ``` Enable ```
  - Hosting A Static Website ``` Click ```
  - Index Document section, add ``` index.html ```
  ![](./README_Docs/edit_wbsite_1.png)
  ![](./README_Docs/edit_wbsite_2.png)


6. Review Url for your File/Website
  - Visit Property Tab once One 
  - Scroll Down to review your url and click to preview
  ![](./README_Docs/url_access_page.png)
  ![](./README_Docs/url_link.png)


7.  :rocket: WEBSITE Hosted
  ![](./README_Docs/successful_url.png)


8. :weary: Error Page 
  - If you get the below error please visit ```Step 5``` or ``` step 1 ```
![](./README_Docs/error_url_page.png)

### :arrow_right: Next We Visit AWS IAM Policy 



``` --- ``` ``` --- ``` ``` --- ```
 ### :fireworks: Star and watch for more
![](./README_Docs/rating.png)