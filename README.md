# AWS Elastic Beanstalk+WordPress：企業級網站架設實務 參考資料

<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->
**Table of Contents**  *generated with [DocToc](https://github.com/thlorenz/doctoc)*

- [推薦序](#%E6%8E%A8%E8%96%A6%E5%BA%8F)
- [本書適合對象](#%E6%9C%AC%E6%9B%B8%E9%81%A9%E5%90%88%E5%B0%8D%E8%B1%A1)
- [第1章:實際營運中的WordPress](#%E7%AC%AC1%E7%AB%A0%E5%AF%A6%E9%9A%9B%E7%87%9F%E9%81%8B%E4%B8%AD%E7%9A%84wordpress)
  - [1-2:為何選用雲端服務](#1-2%E7%82%BA%E4%BD%95%E9%81%B8%E7%94%A8%E9%9B%B2%E7%AB%AF%E6%9C%8D%E5%8B%99)
- [第2章:簡介AWS](#%E7%AC%AC-2-%E7%AB%A0-%09%E7%B0%A1%E4%BB%8Baws)
  - [2-1:簡介AWS](#2-1-%09%E7%B0%A1%E4%BB%8Baws)
  - [2-2: 為何選用AWS](#2-2-%09%E7%82%BA%E4%BD%95%E9%81%B8%E7%94%A8aws)
  - [2-3: 	AWS基本觀念Region與AZ](#2-3-%09aws%E5%9F%BA%E6%9C%AC%E8%A7%80%E5%BF%B5region%E8%88%87az)
- [第 3 章: 	使用AWS準備動作](#%E7%AC%AC-3-%E7%AB%A0-%09%E4%BD%BF%E7%94%A8aws%E6%BA%96%E5%82%99%E5%8B%95%E4%BD%9C)
  - [3-1: 	註冊一個AWS帳號](#3-1-%09%E8%A8%BB%E5%86%8A%E4%B8%80%E5%80%8Baws%E5%B8%B3%E8%99%9F)
  - [3-2: 	Root帳號控管](#3-2-%09root%E5%B8%B3%E8%99%9F%E6%8E%A7%E7%AE%A1)
  - [3-3: 	新增登入帳戶](#3-3-%09%E6%96%B0%E5%A2%9E%E7%99%BB%E5%85%A5%E5%B8%B3%E6%88%B6)
  - [3-4: 	簡介IAM](#3-4-%09%E7%B0%A1%E4%BB%8Biam)
- [第 4 章: 	規劃WordPress在AWS上的網路環境](#%E7%AC%AC-4-%E7%AB%A0-%09%E8%A6%8F%E5%8A%83wordpress%E5%9C%A8aws%E4%B8%8A%E7%9A%84%E7%B6%B2%E8%B7%AF%E7%92%B0%E5%A2%83)
  - [4-1: 	簡介VPC](#4-1-%09%E7%B0%A1%E4%BB%8Bvpc)
- [第 5 章: 	幫WordPress建立DB](#%E7%AC%AC-5-%E7%AB%A0-%09%E5%B9%ABwordpress%E5%BB%BA%E7%AB%8Bdb)
  - [5-1: 	簡介RDS](#5-1-%09%E7%B0%A1%E4%BB%8Brds)
  - [5-3: 	修改RDS的Security Group](#5-3-%09%E4%BF%AE%E6%94%B9rds%E7%9A%84security-group)
- [第 6 章: 	簡介Elastic Compute Cloud](#%E7%AC%AC-6-%E7%AB%A0-%09%E7%B0%A1%E4%BB%8Belastic-compute-cloud)
  - [6-1: 	簡介EC2](#6-1-%09%E7%B0%A1%E4%BB%8Bec2)
    - [6-1-1	自帶硬碟與EBS](#6-1-1%09%E8%87%AA%E5%B8%B6%E7%A1%AC%E7%A2%9F%E8%88%87ebs)
    - [6-1-2	EC2的生命週期](#6-1-2%09ec2%E7%9A%84%E7%94%9F%E5%91%BD%E9%80%B1%E6%9C%9F)
  - [6-2: 	簡介ELB](#6-2-%09%E7%B0%A1%E4%BB%8Belb)
  - [6-3: 	簡介ASG](#6-3-%09%E7%B0%A1%E4%BB%8Basg)
  - [6-4: 	簡介Elastic Beanstalk](#6-4-%09%E7%B0%A1%E4%BB%8Belastic-beanstalk)
    - [6-4-1	內鍵EC2、ELB與ASG與完整監控和報警機制](#6-4-1%09%E5%85%A7%E9%8D%B5ec2elb%E8%88%87asg%E8%88%87%E5%AE%8C%E6%95%B4%E7%9B%A3%E6%8E%A7%E5%92%8C%E5%A0%B1%E8%AD%A6%E6%A9%9F%E5%88%B6)
- [第 7 章: 	架設Elastic Beanstalk](#%E7%AC%AC-7-%E7%AB%A0-%09%E6%9E%B6%E8%A8%ADelastic-beanstalk)
  - [7-2: 	準備WordPress的安裝包](#7-2-%09%E6%BA%96%E5%82%99wordpress%E7%9A%84%E5%AE%89%E8%A3%9D%E5%8C%85)
  - [7-3: 	架設Elastic Beanstalk的環境](#7-3-%09%E6%9E%B6%E8%A8%ADelastic-beanstalk%E7%9A%84%E7%92%B0%E5%A2%83)
  - [7-4: 	連接WordPress所需的DB](#7-4-%09%E9%80%A3%E6%8E%A5wordpress%E6%89%80%E9%9C%80%E7%9A%84db)
- [第 8 章: 	上傳檔案到Elastic Beanstalk的環境](#%E7%AC%AC-8-%E7%AB%A0-%09%E4%B8%8A%E5%82%B3%E6%AA%94%E6%A1%88%E5%88%B0elastic-beanstalk%E7%9A%84%E7%92%B0%E5%A2%83)
  - [8-2: 	安裝WordPress外掛（Plugins）](#8-2-%09%E5%AE%89%E8%A3%9Dwordpress%E5%A4%96%E6%8E%9Bplugins)
  - [8-3: 	使用EB CLI加速原始碼部署](#8-3-%09%E4%BD%BF%E7%94%A8eb-cli%E5%8A%A0%E9%80%9F%E5%8E%9F%E5%A7%8B%E7%A2%BC%E9%83%A8%E7%BD%B2)
    - [8-3-1	安裝EB CLI](#8-3-1%09%E5%AE%89%E8%A3%9Deb-cli)
    - [8-3-2	設定EB CLI的IAM權限](#8-3-2%09%E8%A8%AD%E5%AE%9Aeb-cli%E7%9A%84iam%E6%AC%8A%E9%99%90)
    - [8-3-3	初始化EB CLI](#8-3-3%09%E5%88%9D%E5%A7%8B%E5%8C%96eb-cli)
    - [8-3-4	使用EB CLI上傳檔案](#8-3-4%09%E4%BD%BF%E7%94%A8eb-cli%E4%B8%8A%E5%82%B3%E6%AA%94%E6%A1%88)
  - [8-4: 	結合Git使用](#8-4-%09%E7%B5%90%E5%90%88git%E4%BD%BF%E7%94%A8)
    - [8-4-1	切換develop與master](#8-4-1%09%E5%88%87%E6%8F%9Bdevelop%E8%88%87master)
    - [8-4-2	EB CLI搭配git的部署（deploy）](#8-4-2%09eb-cli%E6%90%AD%E9%85%8Dgit%E7%9A%84%E9%83%A8%E7%BD%B2deploy)
- [第 9 章: 	加速傳輸你網站的多媒體內容](#%E7%AC%AC-9-%E7%AB%A0-%09%E5%8A%A0%E9%80%9F%E5%82%B3%E8%BC%B8%E4%BD%A0%E7%B6%B2%E7%AB%99%E7%9A%84%E5%A4%9A%E5%AA%92%E9%AB%94%E5%85%A7%E5%AE%B9)
- [9-2: 	簡介CloudFront](#9-2-%09%E7%B0%A1%E4%BB%8Bcloudfront)
- [9-3: 	多媒體內容上傳到S3並使用CloudFront 加速](#9-3-%09%E5%A4%9A%E5%AA%92%E9%AB%94%E5%85%A7%E5%AE%B9%E4%B8%8A%E5%82%B3%E5%88%B0s3%E4%B8%A6%E4%BD%BF%E7%94%A8cloudfront-%E5%8A%A0%E9%80%9F)
  - [9-3-1	新建S3 Bucket](#9-3-1%09%E6%96%B0%E5%BB%BAs3-bucket)
  - [9-3-3	建立存取S3的權限設定](#9-3-3%09%E5%BB%BA%E7%AB%8B%E5%AD%98%E5%8F%96s3%E7%9A%84%E6%AC%8A%E9%99%90%E8%A8%AD%E5%AE%9A)
  - [9-3-5	安裝WP Offload S3外掛](#9-3-5%09%E5%AE%89%E8%A3%9Dwp-offload-s3%E5%A4%96%E6%8E%9B)
- [第 10 章: 	幫網站做域名綁定](#%E7%AC%AC-10-%E7%AB%A0-%09%E5%B9%AB%E7%B6%B2%E7%AB%99%E5%81%9A%E5%9F%9F%E5%90%8D%E7%B6%81%E5%AE%9A)
  - [10-1: 	簡介Route53](#10-1-%09%E7%B0%A1%E4%BB%8Broute53)
- [第 11 章: 	申請SSL憑證，讓WordPress使用https](#%E7%AC%AC-11-%E7%AB%A0-%09%E7%94%B3%E8%AB%8Bssl%E6%86%91%E8%AD%89%E8%AE%93wordpress%E4%BD%BF%E7%94%A8https)
  - [11-1: 	簡介ACM](#11-1-%09%E7%B0%A1%E4%BB%8Bacm)
  - [11-2: 	使用ACM申請SSL憑證](#11-2-%09%E4%BD%BF%E7%94%A8acm%E7%94%B3%E8%AB%8Bssl%E6%86%91%E8%AD%89)
- [第 12 章: 	寄送不會被放到垃圾信的系統信件](#%E7%AC%AC-12-%E7%AB%A0-%09%E5%AF%84%E9%80%81%E4%B8%8D%E6%9C%83%E8%A2%AB%E6%94%BE%E5%88%B0%E5%9E%83%E5%9C%BE%E4%BF%A1%E7%9A%84%E7%B3%BB%E7%B5%B1%E4%BF%A1%E4%BB%B6)
  - [12-2: 	申請SES](#12-2-%09%E7%94%B3%E8%AB%8Bses)
  - [12-3: 	設定WordPress SMTP來寄信](#12-3-%09%E8%A8%AD%E5%AE%9Awordpress-smtp%E4%BE%86%E5%AF%84%E4%BF%A1)
- [第 13 章: 	開發協同合作與上線部署](#%E7%AC%AC-13-%E7%AB%A0-%09%E9%96%8B%E7%99%BC%E5%8D%94%E5%90%8C%E5%90%88%E4%BD%9C%E8%88%87%E4%B8%8A%E7%B7%9A%E9%83%A8%E7%BD%B2)
  - [13-2: 	藍綠燈部署避免環境升級停機](#13-2-%09%E8%97%8D%E7%B6%A0%E7%87%88%E9%83%A8%E7%BD%B2%E9%81%BF%E5%85%8D%E7%92%B0%E5%A2%83%E5%8D%87%E7%B4%9A%E5%81%9C%E6%A9%9F)
- [第 14 章: 	隨時掌控你網站的狀態](#%E7%AC%AC-14-%E7%AB%A0-%09%E9%9A%A8%E6%99%82%E6%8E%8C%E6%8E%A7%E4%BD%A0%E7%B6%B2%E7%AB%99%E7%9A%84%E7%8B%80%E6%85%8B)
  - [14-1: 	使用Elastic Beanstalk監控](#14-1-%09%E4%BD%BF%E7%94%A8elastic-beanstalk%E7%9B%A3%E6%8E%A7)
  - [14-2: 	運用CloudWatch監控RDS](#14-2-%09%E9%81%8B%E7%94%A8cloudwatch%E7%9B%A3%E6%8E%A7rds)
  - [14-4: 	使用CloudWatch Logs監控access_log並偵測XML-RPC攻擊](#14-4-%09%E4%BD%BF%E7%94%A8cloudwatch-logs%E7%9B%A3%E6%8E%A7access_log%E4%B8%A6%E5%81%B5%E6%B8%ACxml-rpc%E6%94%BB%E6%93%8A)
    - [14-4-1	同步access_log到CloudWatch Logs](#14-4-1%09%E5%90%8C%E6%AD%A5access_log%E5%88%B0cloudwatch-logs)
    - [14-4-2	過濾XML-RPC攻擊](#14-4-2%09%E9%81%8E%E6%BF%BExml-rpc%E6%94%BB%E6%93%8A)
- [第 15 章: 	掌控AWS花費](#%E7%AC%AC-15-%E7%AB%A0-%09%E6%8E%8C%E6%8E%A7aws%E8%8A%B1%E8%B2%BB)
  - [15-1: 	隨需付費方式與預留執行付費方式](#15-1-%09%E9%9A%A8%E9%9C%80%E4%BB%98%E8%B2%BB%E6%96%B9%E5%BC%8F%E8%88%87%E9%A0%90%E7%95%99%E5%9F%B7%E8%A1%8C%E4%BB%98%E8%B2%BB%E6%96%B9%E5%BC%8F)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->


## 推薦序
- AWS Community Hero - [Cliff Lu](https://aws.amazon.com/tw/heroes/asia-pacific/clifflu/)

## 本書適合對象
- 如果你只想要打造個人網站，玩玩EC2+AWS，可以參考：[http://docs.aws.amazon.com/zh_cn/AWSEC2/latest/UserGuide/hosting-wordpress.html](http://docs.aws.amazon.com/zh_cn/AWSEC2/latest/UserGuide/hosting-wordpress.html)

## 第1章:實際營運中的WordPress
### 1-2:為何選用雲端服務
- 註1: [Youtube - 011 翟本喬,吳志偉 A virtual storage appliance based on GlusterFS and OpenStack](https://www.youtube.com/watch?v=0w0t1Jo5mEs)
- 註3: [Amazon RDS 僅供讀取複本](https://aws.amazon.com/tw/rds/details/read-replicas/)
- 註4: [Amazon RDS 異地同步備份部署](https://aws.amazon.com/tw/rds/details/multi-az/)

## 第 2 章: 簡介AWS
### 2-1: 簡介AWS 
- 註1: [Quora - 什麼是AWS的第一個公開服務](https://www.quora.com/What-was-the-first-AWS-service)
- 註2: [SlideShare - AWS服務的成長速度](http://www.slideshare.net/AmazonWebServices/awsome-day-2016-module-1-aws-introduction-and-history001-aws-introduction-and-history-sjcole)
- 註3: [SlideShare - 截至2016年AWS所提供的服務個數](http://www.slideshare.net/AmazonWebServices/awsome-day-2016-module-1-aws-introduction-and-history001-aws-introduction-and-history-sjcole)

### 2-2: 	為何選用AWS
- 註4: [Gartner從2011年開始評比AWS是第一名的雲端服務](http://jroller.com/MasterMark/entry/csc_in_the_leaders_quadrant)
- 註5: [Gartner 2016 雲端服務評比](https://goo.gl/UYmZ5R)
- 註6: [Netflix Case Study](https://aws.amazon.com/solutions/case-studies/netflix/)
- 註7: [Netflix Open Source Software Center](https://netflix.github.io/)
- 註8: [Supercell Case Study](https://aws.amazon.com/solutions/case-studies/supercell/)
- 註9: [Suercell使用者達到一億人](https://twitter.com/ipaananen/status/706844089216532480)
- 註10: [AWS線上文件](https://aws.amazon.com/documentation/)
- 註11: [AWS白皮書](https://aws.amazon.com/tw/whitepapers/)

### 2-3: 	AWS基本觀念Region與AZ
- 註12: [AWS 全球基礎設施](https://aws.amazon.com/tw/about-aws/global-infrastructure/)
- 註13: [AWS 全球Region](https://aws.amazon.com/tw/about-aws/global-infrastructure/)
- 註14: [SlideShare - AWS Region與AZ示意圖](http://www.slideshare.net/AmazonWebServices/awsome-day-2016-module-1-aws-introduction-and-history001-aws-introduction-and-history-sjcole)
- 註15: [AWS Edge Locations](https://aws.amazon.com/cloudfront/details/)

## 第 3 章: 	使用AWS準備動作
### 3-1: 	註冊一個AWS帳號
- [AWS帳號註冊](https://portal.aws.amazon.com/gp/aws/developer/registration/index.html)

### 3-2: 	Root帳號控管
- 註1: [Google Authenticator](https://aws.amazon.com/tw/iam/details/mfa/)

### 3-3: 	新增登入帳戶
- 註2: [AWS IAM Best Practice](http://docs.aws.amazon.com/IAM/latest/UserGuide/best-practices.html)

### 3-4: 	簡介IAM
- 註3: [SlideShare - IAM Policy示意圖](http://www.slideshare.net/AmazonWebServices/awsome-day-2016-module-3-security-identity-and-access-management)
- 註4: [AWS IAM 線上文件](https://aws.amazon.com/documentation/iam/)

## 第 4 章: 	規劃WordPress在AWS上的網路環境
### 4-1: 	簡介VPC
- 註1: [AWS VPC線上文件](https://aws.amazon.com/documentation/vpc/)
- 註2: [Cliff文章：AWS VPC 心得](https://blog.clifflu.net/blog/2013/10/aws-vpc-%E5%BF%83%E5%BE%97/)

## 第 5 章: 	幫WordPress建立DB
### 5-1: 	簡介RDS
- 註1: [Amazon RDS 僅供讀取複本](https://aws.amazon.com/tw/rds/details/read-replicas/)
- 註2: [Amazon RDS 異地同步備份部署](https://aws.amazon.com/tw/rds/details/multi-az/)

### 5-3: 	修改RDS的Security Group
- 註3: [SlideShare - Security Group示意圖](http://www.slideshare.net/AmazonWebServices/awsome-day-2016-module-3-security-identity-and-access-management)

## 第 6 章: 	簡介Elastic Compute Cloud

### 6-1: 	簡介EC2
#### 6-1-1	自帶硬碟與EBS
- 註1: [AWS Dedicated Hosts](https://aws.amazon.com/tw/ec2/dedicated-hosts/)

#### 6-1-2	EC2的生命週期
- 註2: [AWS Elastic IP Address](http://docs.aws.amazon.com/AWSEC2/latest/UserGuide/elastic-ip-addresses-eip.html)
- 註3: [EC2生命週期示意圖](http://www.slideshare.net/AmazonWebServices/awsome-day-2016-module-2-infrastructure-services)

### 6-2: 	簡介ELB
- 註4: [ELB示意圖](http://www.slideshare.net/AmazonWebServices/awsome-day-2016-module-5-aws-elasticity-and-management-tools)
- 註5: [AWS Shiled](https://aws.amazon.com/tw/shield/)
- 註6: [AWS Shiled費用](https://aws.amazon.com/tw/shield/pricing/)
- 註7: [AWS Shiled基本方案可阻擋96%的DDoS攻擊](https://aws.amazon.com/tw/blogs/aws/aws-shield-protect-your-applications-from-ddos-attacks/)
- 註8: [AWS WAF](https://aws.amazon.com/tw/waf/)

### 6-3: 	簡介ASG
- 註9: [ASG裡的EC2生命週期示意圖](http://www.slideshare.net/AmazonWebServices/awsome-day-2016-module-5-aws-elasticity-and-management-tools)
- 註10: [ASG最大最小值示意圖](http://www.slideshare.net/AmazonWebServices/awsome-day-2016-module-5-aws-elasticity-and-management-tools)

### 6-4: 	簡介Elastic Beanstalk
#### 6-4-1	內鍵EC2、ELB與ASG與完整監控和報警機制
- 註11: [AWS CloudFormation](https://aws.amazon.com/tw/cloudformation/)
- 註13: [Elastic Beanstalk幫你建構出完整的環境示意圖](http://www.slideshare.net/AmazonWebServices/dvo201-scaling-your-web-applications-with-aws-elastic-beanstalk)
- 註14: [AWS CloudWatch](https://aws.amazon.com/tw/cloudwatch/)

## 第 7 章: 	架設Elastic Beanstalk
### 7-2: 	準備WordPress的安裝包
- [AWS 官方文件 - 用Elastic Beanstalk架WordPress之下載WordPress](http://docs.aws.amazon.com/getting-started/latest/wordpress/download-wordpress.html)
- [WordPress 安裝包下載](http://wordpress.org/download/)
- 編輯[wp-config.php](src/wp-config.php), DB資訊部份，修改以下程式碼

找到以下
```php
define('DB_NAME', 'database_name_here');
define('DB_USER', 'username_here');
define('DB_PASSWORD', 'password_here');
define('DB_HOST', 'localhost');
```

把它改為
```php
define('DB_NAME',     $_SERVER["RDS_DB_NAME"]);
define('DB_USER',     $_SERVER["RDS_USERNAME"]);
define('DB_PASSWORD', $_SERVER["RDS_PASSWORD"]);
define('DB_HOST',     $_SERVER["RDS_HOSTNAME"]);
```

- 編輯wp-config.php, 安全性的設定，修改以下程式碼

找到以下
```php
define('AUTH_KEY',         'put your unique phrase here');
define('SECURE_AUTH_KEY',  'put your unique phrase here');
define('LOGGED_IN_KEY',    'put your unique phrase here');
define('NONCE_KEY',        'put your unique phrase here');
define('AUTH_SALT',        'put your unique phrase here');
define('SECURE_AUTH_SALT', 'put your unique phrase here');
define('LOGGED_IN_SALT',   'put your unique phrase here');
define('NONCE_SALT',       'put your unique phrase here');
```

把它改為
```php
define('AUTH_KEY',         $_SERVER["AUTH_KEY"]);
define('SECURE_AUTH_KEY',  $_SERVER["SECURE_AUTH_KEY"]);
define('LOGGED_IN_KEY',    $_SERVER["LOGGED_IN_KEY"]);
define('NONCE_KEY',        $_SERVER["NONCE_KEY"]);
define('AUTH_SALT',        $_SERVER["AUTH_SALT"]);
define('SECURE_AUTH_SALT', $_SERVER["SECURE_AUTH_SALT"]);
define('LOGGED_IN_SALT',   $_SERVER["LOGGED_IN_SALT"]);
define('NONCE_SALT',       $_SERVER["NONCE_SALT"]);
```

- 加入以下程式讓URL從設定檔讀取

```php
define('WP_SITEURL', 'http://' . $_SERVER['HTTP_HOST'] . '/');
define('WP_HOME', 'http://' . $_SERVER['HTTP_HOST'] . '/');
```

- 在Mac OS X或其他Linux的環境壓縮wordpress-x.y.z.zip的命令
```
zip -r ../wordpress-x.y.z.zip .
```

### 7-3: 	架設Elastic Beanstalk的環境
- [AWS 官方文件 - 用Elastic Beanstalk架WordPress之上傳WordPress](http://docs.aws.amazon.com/getting-started/latest/wordpress/deploy-wordpress-on-aws.html)
- 註1: [AWS Elastic Beanstalk不同的Deployment Policy](https://docs.aws.amazon.com/elasticbeanstalk/latest/dg/using-features.rolling-version-deploy.html)

### 7-4: 	連接WordPress所需的DB
- [WordPress Salt產生器](https://api.wordpress.org/secret-key/1.1/salt/)

## 第 8 章: 	上傳檔案到Elastic Beanstalk的環境
### 8-2: 	安裝WordPress外掛（Plugins）
- [Elastic Beanstalk Application Update]( http://docs.aws.amazon.com/getting-started/latest/wordpress/update-application-version.html)
- [Amazon Web Service WordPress外掛](https://downloads.wordpress.org/plugin/amazon-web-services.1.0.zip)
- 防止客戶自行安裝plugins或themes，可在[wp-config.php](src/wp-config.php)裡加入
```php
define('DISALLOW_FILE_MODS',true);
```
- 註3: [將PHP Session儲存在DB的作法](http://docstore.mik.ua/orelly/webprog/pcook/ch08_07.htm)
- 註4: [在Elastic Beanstalk環境中修改php.ini的作法](http://docs.aws.amazon.com/elasticbeanstalk/latest/dg/create_deploy_PHP.container.html#php-configuration-namespace)
- 註5: [ELB Session Stickiness](https://aws.amazon.com/tw/blogs/aws/new-elastic-load-balancing-feature-sticky-sessions/)

### 8-3: 	使用EB CLI加速原始碼部署
#### 8-3-1	安裝EB CLI
- 註6: [Elastic Beanstalk CLI安裝官方文件](http://docs.aws.amazon.com/elasticbeanstalk/latest/dg/eb-cli3-install.html)
- 註7: [下載Python](https://www.python.org/downloads/)
- 註8: [安裝pip](https://pip.pypa.io/en/stable/installing/)
- 使用 `pip` 安裝 `awsebcli`
```
$ pip install --upgrade --user awsebcli
```
- 在Linux下把eb加到PATH環境變數

Step 1. 找到shell
```
$ ls -a ~
```
Step 2. 加到shell
```shell
export PATH=~/.local/bin:$PATH
```
Step 3. 載入profile
```
$ source ~/.bash_profile
```
Step 4. 檢驗eb cli是否有成功
```
$ eb --version
EB CLI 3.8.4 （Python 2.7.1）
```
#### 8-3-2	設定EB CLI的IAM權限
- 註9: [把AWS keys放在GitHub上的杯具](http://www.theregister.co.uk/2015/01/06/dev_blunder_shows_github_crawling_with_keyslurping_bots/)
- 註10: [AWS Best Practices for Managing AWS Access Keys](http://docs.aws.amazon.com/general/latest/gr/aws-access-keys-best-practices.html)

#### 8-3-3	初始化EB CLI
- 初始化命令: `eb init`

#### 8-3-4	使用EB CLI上傳檔案
- 參考修改後的[.htaccess](src/.htaccess)
- [WordPress Basic WP的.htaccess內容](https://codex.wordpress.org/htaccess)
```
# BEGIN WordPress
<IfModule mod_rewrite.c>
RewriteEngine On
RewriteBase /
RewriteRule ^index\.php$ - [L]
RewriteCond %{REQUEST_FILENAME} !-f
RewriteCond %{REQUEST_FILENAME} !-d
RewriteRule . /index.php [L]
</IfModule>
# END WordPress
```
### 8-4: 	結合Git使用
#### 8-4-1	切換develop與master
- 註11: [Git開發流程模式](http://nvie.com/posts/a-successful-git-branching-model/)

#### 8-4-2	EB CLI搭配git的部署（deploy）
- 只deploy還在staging區的code
Step 1. git add to staged area
```
~/eb$ git add .
```

Step 2. eb deploy staged area code
```
~/eb$ eb deploy --staged
```

## 第 9 章: 	加速傳輸你網站的多媒體內容
## 9-2: 	簡介CloudFront
- 註1: [AWS全球 Edge Location](https://aws.amazon.com/tw/cloudfront/details/#edge-locations)
- 註2: [AWS CloudFront後端串接客製化URL](http://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/DownloadDistS3AndCustomOrigins.html#concept_CustomOrigin)
- 註3: [AWS CloudFront支援串流影音](http://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/distribution-rtmp.html)
- 註4: [AWS WAF](https://aws.amazon.com/tw/waf/)
- 註5: [利用AWS WAF抵檔DDoS](http://docs.aws.amazon.com/waf/latest/developerguide/ddos-overview.html)

## 9-3: 	多媒體內容上傳到S3並使用CloudFront 加速
### 9-3-1	新建S3 Bucket
- 註6: [S3 Bucket與Object示意圖](http://www.slideshare.net/AmazonWebServices/awsome-day-2016-module-2-infrastructure-services)

### 9-3-3	建立存取S3的權限設定
- 註7: [WP Offload S3所需要的IAM權限](https://deliciousbrains.com/wp-offload-s3/doc/quick-start-guide/)
```json
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Effect": "Allow",
      "Action": [
        "s3:CreateBucket",
        "s3:DeleteObject",
        "s3:Put*",
        "s3:Get*",
        "s3:List*"
      ],
      "Resource": [
        "arn:aws:s3:::*"
      ]
    }
  ]
}
```

### 9-3-5	安裝WP Offload S3外掛
- 註8: [AWS官方文件教如何使用W3 Total Cache將圖送到CloudFront](http://docs.aws.amazon.com/getting-started/latest/wordpress/deploy-wordpress-on-aws.html)
- 註9: [W3 Total Cache](https://wordpress.org/plugins/w3-total-cache/)
- 註10: [WP Offload S3](https://deliciousbrains.com/wp-offload-s3/)
- 註9-3-4: [W3 Total Cache外掛](https://wordpress.org/plugins/w3-total-cache/)
- 編輯[wp-config.php](src/wp-config.php)將AWS Key傳入

```php
/**
* AWS plugin key setting
*/
define( 'DBI_AWS_ACCESS_KEY_ID', $_SERVER['AWS_ACCESS_KEY_ID'] );
define( 'DBI_AWS_SECRET_ACCESS_KEY', $_SERVER['AWS_SECRET_ACCESS_KEY'] );
```

## 第 10 章: 	幫網站做域名綁定
### 10-1: 	簡介Route53
- 註1: [AWS Route53 權重分流(Weighted Routing)](http://docs.aws.amazon.com/Route53/latest/DeveloperGuide/routing-policy.html#routing-policy-weighted)
- 註2: [AWS Route53 依延遲時間為依據的分流(Latency-Based Routing)](http://docs.aws.amazon.com/Route53/latest/DeveloperGuide/routing-policy.html#routing-policy-latency)
- 註3: [AWS Rotue53 依所處的地理位置來做的分流(Geolocation Routing)](http://docs.aws.amazon.com/Route53/latest/DeveloperGuide/routing-policy.html#routing-policy-geo)
- 註4: [AWS宣佈支援倫敦區](https://aws.amazon.com/tw/about-aws/whats-new/2016/12/announcing-the-aws-europe-london-region/)

## 第 11 章: 	申請SSL憑證，讓WordPress使用https
### 11-1: 	簡介ACM
- 註1: [AWS ACM 價錢](https://aws.amazon.com/tw/certificate-manager/pricing/) 
- 註2: [AWS ACM 會自動幫你renew certificate並deploy至ELB](https://aws.amazon.com/tw/certificate-manager/faqs/)
- 註3: [AWS ACM 朝匯入現存的certificate](http://docs.aws.amazon.com/acm/latest/userguide/import-certificate.html)

### 11-2: 	使用ACM申請SSL憑證
- 編輯[wp-config.php](src/wp-config.php)讓網站支援SSL
加在檔案前面
```
if (( $_SERVER['HTTP_CLOUDFRONT_FORWARDED_PROTO'] == 'https' ) || ( $_SERVER['HTTP_X_FORWARDED_PROTO'] == 'https' )) {
 $_SERVER['HTTPS'] = 'on';
}
```

另外找到以下程式碼，把http改成https
```
define('WP_SITEURL', 'https://' . $_SERVER['HTTP_HOST'] . '/');
define('WP_HOME', 'https://' . $_SERVER['HTTP_HOST'] . '/');
```

## 第 12 章: 	寄送不會被放到垃圾信的系統信件
### 12-2: 	申請SES 
- 註1: [處理SES Bounces and Complaints](http://docs.aws.amazon.com/ses/latest/DeveloperGuide/best-practices-bounces-complaints.html)
- [WP Mail SMTP](https://wordpress.org/plugins/wp-mail-smtp/)

### 12-3: 	設定WordPress SMTP來寄信
- [WP Mail SMTP plugin](https://wordpress.org/plugins/wp-mail-smtp/)

## 第 13 章: 	開發協同合作與上線部署
### 13-2: 	藍綠燈部署避免環境升級停機
- 註1: [Youtube - AWS re:Invent 2015 | (DVO401) Deep Dive into Blue/Green Deployments on AWS](https://www.youtube.com/watch?v=aX54mhZbN58)


## 第 14 章: 	隨時掌控你網站的狀態
### 14-1: 	使用Elastic Beanstalk監控
- 註1: [CloudWatch Metrics](http://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/viewing_metrics_with_cloudwatch.html)

### 14-2: 	運用CloudWatch監控RDS
- 註2: [Monitoring Amazon RDS](http://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/CHAP_Monitoring.html)

### 14-4: 	使用CloudWatch Logs監控access_log並偵測XML-RPC攻擊
#### 14-4-1	同步access_log到CloudWatch Logs
- 註3: [AWS CloudWatch 價格](https://aws.amazon.com/tw/cloudwatch/pricing/)

#### 14-4-2	過濾XML-RPC攻擊
- 註4: [AWS CloudWatch Logs的Filter Pattern](http://docs.aws.amazon.com/AmazonCloudWatch/latest/logs/FilterAndPatternSyntax.html)
- 註5: [Cerber Security & Limit Login Attempts WordPress Plugin](https://wordpress.org/plugins/wp-cerber/)
- 註6: [關閉WordPress XML-RPC](http://wordpress.blog.tw/disable-xml-rpc/)
- 註7: [How to Configure Rate-Based Blacklisting with AWS WAF and AWS Lambda](https://aws.amazon.com/tw/blogs/security/how-to-configure-rate-based-blacklisting-with-aws-waf-and-aws-lambda/)

## 第 15 章: 	掌控AWS花費
### 15-1: 	隨需付費方式與預留執行付費方式
- 註1: [EC2計費模式](https://aws.amazon.com/tw/ec2/pricing/)
- 註2: [在AWS Marketplace賣EC2 Reserved Instance](http://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ri-market-selling-guide.html)
- 註3: [預留EC2實的費用](https://aws.amazon.com/tw/ec2/pricing/reserved-instances/pricing/)
- 