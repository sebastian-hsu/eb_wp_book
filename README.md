# AWS Elastic Beanstalk+WordPress：企業級網站架設實務(暫定) 參考資料

## 1-2
- 註1-2-1: [011 翟本喬,吳志偉 A virtual storage appliance based on GlusterFS and OpenStack](https://www.youtube.com/watch?v=0w0t1Jo5mEs)
- 註1-2-2: [Amazon RDS 僅供讀取複本](https://aws.amazon.com/tw/rds/details/read-replicas/?nc1=h_ls)
- 註1-2-3: [Amazon RDS 異地同步備份部署](https://aws.amazon.com/tw/rds/details/multi-az/)

## 2-2
- 註2-2-1: [在基礎設施即服務 (IaaS) Magic Quadrant 報告中，AWS 連續六年被評為領導者](https://goo.gl/UYmZ5R)
- 註2-2-2: [Netflix Case Study](https://aws.amazon.com/solutions/case-studies/netflix/)
- 註2-2-3: [Netflix Open Source Software Center](https://netflix.github.io/)
- 註2-2-4: [Supercell Case Study](https://aws.amazon.com/solutions/case-studies/supercell/)
- 註2-2-5: [Suercell 100 Million Users](https://twitter.com/ipaananen/status/706844089216532480)
- 註2-2-6: [AWS使用文件](https://aws.amazon.com/documentation/)

## 2-3
- 註2-3-1: [AWS 全球基礎設施](https://aws.amazon.com/tw/about-aws/global-infrastructure/)

## 3-1
- [AWS帳號註冊](https://portal.aws.amazon.com/gp/aws/developer/registration/index.html)

## 3-2
- 註3-2-1: [Google Authenticator](https://aws.amazon.com/tw/iam/details/mfa/)

## 3-4
- 註3-4-1: [IAM Documentation](https://aws.amazon.com/documentation/iam/)

## 4-1
- 註4-1-1: [VPC Documentation](https://aws.amazon.com/documentation/vpc/)

## 7-2
- [AWS 官方文件，用Elastic Beanstalk架WordPress之下載WordPress](http://docs.aws.amazon.com/getting-started/latest/wordpress/download-wordpress.html)
- [WordPress 下載](http://wordpress.org/download/)
- 編輯wp-config.php, DB資訊部份，修改以下程式碼

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


