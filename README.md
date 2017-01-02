# AWS Elastic Beanstalk+WordPress：企業級網站架設實務 參考資料

* auto-gen TOC:
{:toc}

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