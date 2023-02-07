## :rocket: DEPLOYING FROM CIRCLECI PIPELINE TO S3 BUCKET
Here we will be updating our portfolio to github and connect circleci pipeling to deploy to S3 bucket 

### Prerequisite
1. Updating S3 bucket to be hosting our website from  AWS CloudFront
  - :note: When ever we update our file to S3 bucket, we will always need to expose the file to public view which will defeat our automation process.
  - In order to avoid such, we will be using AWS CloudFront for hosting our s3_bucket to Edge Location 

### ⚙️ Steps 1 - Hosting to CloudFront (Edge Location)
- Follow [YOUTUBE VIDEO](https://www.youtube.com/watch?v=-DDGYzKtNwc)
``` OR ```
- Visit AWS and search for CloudFront
![](./images/cloudFront_search.png)

```  ----  ```  ``` --- ``` ``` ---  ``` ``` --- ```

- Create New Cloudfront for your portfolio
![](./images/cloudFront_create.png)

```  ----  ```  ``` --- ``` ``` ---  ``` ``` --- ```

- Coneect your S3 bucket and click enter
![](./images/cloudFront_s3.png)

```  ----  ```  ``` --- ``` ``` ---  ``` ``` --- ```

- Get your CloudFront Url
![](./images/cloudFront_url1.png)

```  ----  ```  ``` --- ``` ``` ---  ``` ``` --- ```

![](./images/cloudFront_url.png)


### ⚙️ Steps 2 - Disable s3_bucket access 
Here we only want access to s3 bucket through cloundfront (CDN)
1. Visit your S3 bucket 
2. Go to the permission tab and proceed
![](./images/s3_bublic_access.png)
![](./images/s3_bublic_access2.png)
![](./images/s3_bublic_access4.png)



```  ----  ```  ``` --- ``` ``` ---  ``` ``` --- ```
```  ----  ```  ``` --- ``` ``` ---  ``` ``` --- ```
```  ----  ```  ``` --- ``` ``` ---  ``` ``` --- ```


### :rocket: Connecting to Circleci
We will now start connection to circleci throug GitHub to AWS S3(CloudFront/Edge location) access

- Create 
  - ``` .circleCi/config.yml ```
  - folder/file in the root of your portfolio

1. Copy the below command and pasted
[CircleCI_PipelineCode](https://github.com/dev-luqman/DevOps_Room/blob/main/.circleci/config.yml)
![](./images/s3_bublic_access4.png)
:book: Beware of indentation


2. Connect to circleCi
![](./images/circleci_home.png)

```  ----  ```  ``` --- ``` ``` ---  ``` ``` --- ```

3. Connect to github project
![](./images/circleci_connect4.png)

```  ----  ```  ``` --- ``` ``` ---  ``` ``` --- ```

4. Sellect the branch and connect
![](./images/circleci_connect.png)

5. At first your pipeline will fail 
![](./images/circleci_failed2.png)

:book: failed as a result of trying to connect aws s3 bucket and found no connection
![](./images/circleci_failed1.png)

6. SetUp a AWS connection 
![](./images/project_setting.png)

```  ----  ```  ``` --- ``` ``` ---  ``` ``` --- ```

![](./images/environment_setting.png)

```  ----  ```  ``` --- ``` ``` ---  ``` ``` --- ```

:book: Add your circleci Ennvironment
![](./images/environment_add.png)

7. getting your aws IAM credentials
####visit AWS CONSOLE
![](./images/iam_credential2.png)

```  ----  ```  ``` --- ``` ``` ---  ``` ``` --- ```

![](./images/iam_credentials3.png)
![](./images/iam_credentials4.png)
![](./images/iam_credentials5.png)
:book: ensure you save token in a note pad because one time access
![](./images/iam_credentials7.png)


```  ----  ```  ``` --- ``` ``` ---  ``` ``` --- ```
```  ----  ```  ``` --- ``` ``` ---  ``` ``` --- ```
```  ----  ```  ``` --- ``` ``` ---  ``` ``` --- ```

8. Let Get back to our pipeline and rerun 

![](./images/circie_rerun.png)
![](./images/circleci_success.png)
![](./images/circleci_success2.png)


9. Update your portfolio and push to github
![](./images/updated_portfolio.png)
![](./images/circleci_Updating.png)
```  ----  ```  ``` --- ``` ``` ---  ``` ``` --- ```
![](./images/rerun_pipeline.png)


10. Check your CLoudfront Url to see the update
![](./images/cloudFront_url1.png)
```  ----  ```  ``` --- ``` ``` ---  ``` ``` --- ```
![](./images/CloudFront2.png)
