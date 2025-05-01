# Insecure Design 

## Introduction 
Insecure design refers to vulnerabilities that are part of an application's architecture from the beginning, not due to poor implementation or configuration. These issues often arise from improper threat modeling during the planning stages. 

## Key Points 
• Insecure design vulnerabilities are rooted in the concept and structure of the application. 

• They can be introduced when developers create "shortcuts" for easier testing, such as disabling security checks like OTP validation. 

• A notable example is Instagram's password reset process, where a 6-digit code is sent via SMS. Although there was rate-limiting, it was only enforced per IP address. 

• An attacker could use multiple IP addresses to brute-force the code, making the attack viable despite the rate-limiting. 

• A total of 4,000 IP addresses would be needed to try all possible combinations of the 6-digit code due to cloud services’ accessibility. 

• This vulnerability highlights a design flaw, as typical users would not have access to many IP addresses for concurrent attempts. 

## Conclusion 
Fixing insecure design vulnerabilities often requires extensive redevelopment. To prevent these issues, it's important to perform threat modeling early in the development lifecycle. For further information on secure development practices, refer to the SSDLC room. 

## Practical Example Try Hack Me
Navigate to http://MACHINE_IP:85 and access joseph's account. Identify the weakness in its password reset process and consider how it can be exploited.

Now This Challenge is based on the Insecure Design Flaw, which basically means we can bruteforce some sort of feature in a website that grant us access to something. In this case,
we are allowed to bruteforce the reset password feature, and by choosing the color, we can easily guess what color is it. In this case was green.

Getting the new password and entering the account we get: THM{Not_3ven_c4tz_c0uld_sav3_U!}.