# s3_static_website
## Getting Started
How i created my static website using s3 service  
1. Create a bucket named "www.sureshvenkey.com"  
2. Nothing to select on "configure option", click Next.    
3. Un select "Block all public access" in "Set Permission"  and procced Next.  
4. Review and finish.

## In addtion to this add a policy as mentioned below  
{
    "Version": "2012-10-17",
    "Statement": [
        {
            "Sid": "PublicReadGetObject",
            "Effect": "Allow",
            "Principal": "*",
            "Action": "s3:GetObject",
            "Resource": "arn:aws:s3:::www.venkatraj.in/*"
        }
    ]
}

## goDaddy 
### First method
Add the CNAME entry in goDaddy for your website i.e. www.sureshvenkey.com
![Image of Yaktocat](https://github.com/sureshvenkey/s3_static_website/blob/master/s3_setting_in_dodaddy.PNG)

### Second method
By forwarding to s3 bucket 

![Image of Yaktocat](https://github.com/sureshvenkey/s3_static_website/blob/master/forwarding_settings.PNG)

Default value you get in DNS A and CNAME records for forward settings.

![Image of Yaktocat](https://github.com/sureshvenkey/s3_static_website/blob/master/default_value_comes_while_forwarding.PNG)

## License
This project is licensed under the MIT License - see the LICENSE.md file for details
