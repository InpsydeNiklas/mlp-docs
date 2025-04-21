---
title: Installation and activation
nav_order: 2
parent: Configure AutoTranslate
has_children: false
---

## Overview

The **Amazon Translate** integration within MultilingualPress enables seamless machine translation for your website. Powered by AWS (Amazon Web Services), Amazon Translate provides translations across 75 languages, tailored to meet your needs. By connecting Amazon Translate, you can automate the translation process for your site's content.

![[Pasted image 20250222235119.png]]

## Key Configuration Steps

1. **Activate Amazon Translate**:
    - To get started, navigate to the AutoTranslate settings in MultilingualPress.
    - Check the **Activate Amazon Translate** box to enable the feature.
2. **Enter AWS Access Key and Secret Access Key**:
    - Amazon Translate requires an Access Key and a Secret Access Key to connect with AWS services.
    - If you don’t have AWS credentials, sign in to your [AWS account](https://aws.amazon.com/) and generate the keys.
    - Enter these keys into the **Access Key** and **Secret Access Key** fields on the Amazon Translate settings page in MultilingualPress.
3. **Select Service Region**:
    - Choose the appropriate AWS **Service Region** from the dropdown (e.g., US East (Ohio), US West, etc.).
    - This region determines where your translation requests will be handled and ensures the best performance for your needs.
4. **Save Changes**:
    - After entering your credentials and selecting the region, click **Save** to apply your configuration.

## Purpose and Use

- **Automatic Translations**:  
    Amazon Translate will automatically translate your site content into the target languages as configured. This reduces the manual workload associated with translation and speeds up the content localization process.
    
- **Multi-Language Support**:  
    Amazon Translate supports up to 75 languages, allowing you to cater to a wide global audience.
    

## Considerations

- **AWS Free Tier**:  
    Amazon Translate offers a **free tier** that includes up to **2 million characters per month** for the first 12 months. Be aware of your usage to avoid extra charges once the free tier expires.
    
- **Accuracy and Context**:  
    While Amazon Translate offers accurate translations, it’s important to verify that the translated content fits the context and tone of your site. Machine translation might need manual corrections for more nuanced or complex content.
    
- **Security**:  
    Ensure that your AWS Access Key and Secret Access Key are securely stored and not exposed in your site’s public code or elsewhere.
    

## Troubleshooting

- **Invalid API Keys**:  
    If the API keys are incorrect or expired, Amazon Translate will fail to process translation requests. Ensure that the keys are valid and correctly entered in the settings.
    
- **Region Mismatch**:  
    If the selected service region doesn’t match your AWS region, translation requests may not be processed correctly. Double-check that the region setting is aligned with your AWS setup.
    

## Conclusion

Integrating Amazon Translate into MultilingualPress simplifies the translation process, offering a powerful solution for creating multilingual websites. By following the setup steps carefully and monitoring usage, you can ensure smooth translations and a great experience for international users.

<!-- Note: I think we should add more images of the AWS setup -->