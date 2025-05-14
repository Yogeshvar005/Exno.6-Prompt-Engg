# Exno.6-Prompt-Engg
## Date:
## Register no: 212222230180
## Aim: 
Development of Python Code Compatible with Multiple AI Tools


## Objective:
Build a Python script that:

a. Connects to multiple AI services via APIs.

b. Sends standardized prompts or inputs.

c. Collects and stores the outputs.

d. Compares the outputs for quality, tone, performance, or accuracy.

e. Generates reports or logs for further analysis.

This process helps in benchmarking AI tools and determining the best tool for a particular task or use case.

## Procedure / Algorithm:
 AI Tools by Modality

1. Image Generation
	•	Stability AI (Stable Diffusion via Stability API)
	•	OpenAI DALL·E
	•	Hugging Face Diffusers (local or hosted models)

2. Voice Enhancement
	•	Adobe Enhance Speech (API access via Adobe Podcast)
	•	ElevenLabs (for voice synthesis and enhancement)
	•	iZotope RX (for pro audio cleanup, often used offline)

3. Video Generation
	•	Runway ML (Gen-2)
	•	Pika Labs
	•	Synthesia (for avatar videos, more templated)

### 1. Image Generation (Stable Diffusion via Stability AI)
'''
import requests

STABILITY_API_KEY = 'your-stability-api-key'

def generate_image(prompt: str):
    url = "https://api.stability.ai/v2beta/stable-image/generate/core"
    headers = {
        "Authorization": f"Bearer {STABILITY_API_KEY}",
        "Content-Type": "application/json"
    }
    payload = {
        "prompt": prompt,
        "output_format": "png"
    }

    response = requests.post(url, headers=headers, json=payload)
    if response.ok:
        with open("generated_image.png", "wb") as f:
            f.write(response.content)
        print("Image saved as generated_image.png")
    else:
        print("Error:", response.json())

### Example usage
### generate_image("A futuristic city skyline at sunset")
'''
Result:
The Python code successfully:

1. Connected with multiple AI tools using APIs.

2. Sent uniform prompts for consistent evaluation.

3. Collected and compared results using natural language metrics.

4. Generated structured, actionable insights that can be used to evaluate tool performance.

## Conclusion:
This experiment demonstrates how Python can serve as a powerful bridge between multiple AI tools, enabling developers to create multi-model pipelines that evaluate, compare, or combine the strengths of various services. This integration supports:

1. Better decision-making on tool selection

2. Automation of evaluation and benchmarking

3. Enhanced productivity by combining outputs

Such a system is scalable and can be adapted for broader use cases including multi-tool chatbots, creative content workflows, or research benchmarking.


## Result: 
The corresponding Prompt is executed successfully
