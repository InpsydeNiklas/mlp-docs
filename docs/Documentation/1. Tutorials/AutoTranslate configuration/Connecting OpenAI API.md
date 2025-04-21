---
title: Connecting OpenAI API
nav_order: 1
parent: Tutorial - Configure AutoTranslate
has_children: false
---
## Overview

The **OpenAI Translate** integration within MultilingualPress leverages OpenAI’s state-of-the-art GPT-based models to deliver outstanding translations across multiple languages. OpenAI captures context and nuances more effectively than many traditional translation tools, making it an ideal choice for producing natural-sounding and accurate translations. OpenAI’s flexible pricing model, which includes both pay-as-you-go and subscription plans, allows businesses to scale their translation needs as they grow.

![[Pasted image 20250222235133.png]]  

## Key Configuration Steps

1. **Activate OpenAI**:
    
    - To get started, navigate to the **AutoTranslate** settings section within MultilingualPress.
    - Check the box labeled **Activate OpenAI** to enable automatic translations using OpenAI.
2. **Enter OpenAI API Key**:
    
    - OpenAI requires an API key for authentication.
    - If you don’t already have one, sign up for an OpenAI account on the [OpenAI platform](https://platform.openai.com/signup) and generate your API key.
    - Once you have the API key, paste it into the **API Key** field under the OpenAI configuration section in MultilingualPress.
3. **Select the Translation Model**:
    
    - OpenAI offers multiple models for translation tasks. The most commonly used model for translation is **GPT-4**.
    - Select the appropriate model for your translation needs. The **GPT-4** model is recommended for high-quality translations.
4. **Save Changes**:
    
    - After entering your API key and selecting the model, click **Save** to activate OpenAI for automatic translations.

## Purpose and Use

- **Automatic Translations**:  
    The OpenAI integration automates the translation process across your website. Once configured, OpenAI will translate content in the target language automatically as it is added or updated on your site.
    
- **High-Quality, Context-Aware Translations**:  
    OpenAI’s GPT-based models provide high-quality translations that capture subtle context and nuances, ensuring the translated text sounds natural and fits the intended meaning.
    

## Considerations

- **Free Trial and Credits**:  
    OpenAI provides **trial credits** to new users, allowing you to explore the service without immediate charges. After the trial, you will need to transition to a **pay-as-you-go model** or select a monthly subscription plan, depending on your translation volume.
    
- **Character Limits and Costs**:  
    Keep track of your character usage and the costs associated with translating large amounts of content. OpenAI’s flexible pricing allows for scaling but be aware of potential charges once trial credits are used up.
    
- **Security**:  
    It’s essential to secure your API key to prevent unauthorized access. Do not expose it in public code repositories or on public-facing parts of your site.
    

## Troubleshooting

- **Invalid API Key**:  
    If your API key is incorrect, OpenAI will fail to process translation requests. Double-check the API key you’ve entered and ensure it’s correct and active.
    
- **Translation Failures**:  
    If translations are not working as expected, verify that your API key is active and that you have sufficient credits or subscription limits. Additionally, check that the correct translation model has been selected.
    

## Conclusion

Integrating OpenAI Translate with MultilingualPress allows you to provide highly accurate, context-sensitive translations across your site. By following the setup steps and securing your API key, you can automate the translation process and create a seamless multilingual experience for your visitors.