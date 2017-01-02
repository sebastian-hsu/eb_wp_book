# AWS Elastic Beanstalk+WordPress：企業級網站架設實務(暫定) 參考資料

## 推薦序
- AWS Community Hero - [Cliff Lu](https://aws.amazon.com/tw/heroes/asia-pacific/clifflu/)

## 本書適合對象
- 如果你只想要打造個人網站，玩玩EC2+AWS，可以參考：[http://docs.aws.amazon.com/zh_cn/AWSEC2/latest/UserGuide/hosting-wordpress.html](http://docs.aws.amazon.com/zh_cn/AWSEC2/latest/UserGuide/hosting-wordpress.html)

## 第 1 章: 	實際營運中的WordPress
### 1-2: 	為何選用雲端服務
- 註1: [Youtube - 011 翟本喬,吳志偉 A virtual storage appliance based on GlusterFS and OpenStack](https://www.youtube.com/watch?v=0w0t1Jo5mEs)
- 註3: [Amazon RDS 僅供讀取複本](https://aws.amazon.com/tw/rds/details/read-replicas/)
- 註4: [Amazon RDS 異地同步備份部署](https://aws.amazon.com/tw/rds/details/multi-az/)

## 第 2 章: 	簡介AWS
### 2-1: 	簡介AWS 
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
- [AWS 官方文件，用Elastic Beanstalk架WordPress之下載WordPress](http://docs.aws.amazon.com/getting-started/latest/wordpress/download-wordpress.html)
- [WordPress 下載](http://wordpress.org/download/)
- 編輯[wp-config.php](src/wp-config.php), DB資訊部份，修改以下程式碼

找到以下
```
define('DB_NAME', 'database_name_here');
define('DB_USER', 'username_here');
define('DB_PASSWORD', 'password_here');
define('DB_HOST', 'localhost');
```

把它改為
```
define('DB_NAME',     $_SERVER["RDS_DB_NAME"]);
define('DB_USER',     $_SERVER["RDS_USERNAME"]);
define('DB_PASSWORD', $_SERVER["RDS_PASSWORD"]);
define('DB_HOST',     $_SERVER["RDS_HOSTNAME"]);
```

- 編輯wp-config.php, 安全性的設定，修改以下程式碼

找到以下
```
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
```
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

```
define('WP_SITEURL', 'http://' . $_SERVER['HTTP_HOST'] . '/');
define('WP_HOME', 'http://' . $_SERVER['HTTP_HOST'] . '/');
```

## 7-3
- [AWS 官方文件，用Elastic Beanstalk架WordPress之上傳WordPress](http://docs.aws.amazon.com/getting-started/latest/wordpress/deploy-wordpress-on-aws.html)

## 7-4
- [WordPress Salt產生器](https://api.wordpress.org/secret-key/1.1/salt/)

## 8-2
- [Elastic Beanstalk Application Update]( http://docs.aws.amazon.com/getting-started/latest/wordpress/update-application-version.html)
- [Amazon Web Service WordPress外掛](https://downloads.wordpress.org/plugin/amazon-web-services.1.0.zip)
- 註8-3-1: [Elastic Beanstalk CLI安裝官方文件](http://docs.aws.amazon.com/elasticbeanstalk/latest/dg/eb-cli3-install.html)
- 註8-3-2: [下載Python](https://www.python.org/downloads/)
- 註8-3-3: [安裝pip](https://pip.pypa.io/en/stable/installing/)
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
  

## 9-2
- 註9-2-1: [AWS全球 Edge Location](https://aws.amazon.com/tw/cloudfront/details/#edge-locations)

## 9-3
- 註9-3-1: [WP Offload S3所需要的IAM權限](https://deliciousbrains.com/wp-offload-s3/doc/quick-start-guide/)

```
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

- 註9-3-2: [WP Offload S3外掛](https://deliciousbrains.com/wp-offload-s3/)
- 註9-3-3: [AWS官方文件教如何使用W3 Total Cache將圖送到CloudFront](http://docs.aws.amazon.com/getting-started/latest/wordpress/deploy-wordpress-on-aws.html)
- 註9-3-4: [W3 Total Cache外掛](https://wordpress.org/plugins/w3-total-cache/)
- 編輯wp-config.php將AWS Key傳入

```
/**
* AWS plugin key setting
*/
define( 'DBI_AWS_ACCESS_KEY_ID', $_SERVER['AWS_ACCESS_KEY_ID'] );
define( 'DBI_AWS_SECRET_ACCESS_KEY', $_SERVER['AWS_SECRET_ACCESS_KEY'] );
```

## 11-2
- 編輯wp-config.php讓網站支援SSL

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

## 12-2
- 註12-2-1: [處理SES Bounces and Complaints](http://docs.aws.amazon.com/ses/latest/DeveloperGuide/best-practices-bounces-complaints.html)
- [WP Mail SMTP](https://wordpress.org/plugins/wp-mail-smtp/)

