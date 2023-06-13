## BurpGPT - Burp Suite ChatGPT Extension

BurpGPT is a Burp Suite extension that combines the power of Burp Suite with OpenAI's GPT (Generative Pre-trained Transformer) models to enhance web application security testing. It enables passive scanning for vulnerability detection and traffic-based analysis by sending web traffic to an OpenAI model specified by the user.

### Features and Advantages
- **Sophisticated Analysis**: BurpGPT leverages OpenAI's GPT models to conduct comprehensive traffic analysis, going beyond security vulnerabilities to detect various issues in scanned applications.
- **Granular Control**: Users can precisely adjust the maximum prompt length to control the number of GPT tokens used in the analysis, allowing for fine-tuned results.
- **Model Flexibility**: BurpGPT offers multiple OpenAI model choices, empowering users to select the one that best suits their needs.
- **Customization**: Users can customize prompts and interact with OpenAI models, opening up limitless possibilities for enhancing web application testing.
- **Seamless Integration**: BurpGPT seamlessly integrates with Burp Suite, providing native features for pre- and post-processing. Analysis results are displayed directly within the Burp UI for efficient analysis.
- **Troubleshooting Support**: The native Burp Event Log facilitates quick resolution of communication issues with the OpenAI API.

### Installation Instructions
1. Install Gradle and ensure it is properly configured.
2. Download BurpGPT by cloning the repository:
```shell
git clone https://github.com/aress31/burpgpt
cd burpgpt
```
3. Build the standalone JAR file using Gradle:
```shell
./gradlew shadowJar
```
4. Load the BurpGPT extension in Burp Suite:
   - Go to "Extension" in Burp Suite.
   - Click on the "Add" button.
   - Select the `burpgpt-all.jar` file located in the `./lib/build/libs` folder.

### How to Use BurpGPT
Before using BurpGPT, follow these steps:

1. Enter a valid OpenAI API key.
2. Select a desired OpenAI model.
3. Define the maximum prompt size. This controls the length of the prompt sent to OpenAI, ensuring it does not exceed the model's token limit (typically around 2048 for GPT-3).
4. Adjust or create custom prompts according to your testing requirements.

Once configured, the Burp passive scanner will send each request to the chosen OpenAI model via the OpenAI API for analysis. The results will be displayed as Informational-level severity findings.

**Note:** BurpGPT requires Java to be installed. If you are using Windows, it is recommended to use Java version 17, as later versions may have bugs. Additionally, ensure you have obtained an API key from OpenAI by visiting their [API key management](https://platform.openai.com/account/api-keys) page.

Feel free to reach out if you have any questions or encounter any issues during the installation or usage of BurpGPT.

Happy testing!

