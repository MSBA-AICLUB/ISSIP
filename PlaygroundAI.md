# Round 2: Playground AI
[Playground AI](https://playground.ai/) is an online AI tool that **generates images and text** in response to user prompts. As the name suggests, the images may have a more **casual tone**. As of now, the tool does not generate videos. Notably, use is limited to **10 prompts a month.**

| Media       | Text       | Image      | Video |
|-------------|------------|------------|-------|
| Supported?  | Yes        | Yes        | No    |
| Rating      | 5          | 3          | 0     |
| Time needed | 10 minutes | 60 minutes | N/A   |

## Getting Started
To start using the tool:
1. Go to https://playground.ai/
2. Click 'Login' and made a new account (Signup with Google didn't work)
3. Follow their tutorial
4. Select a prompt template for Stable Diffusion (the default model)
5. View additional options in Mode: 'Advanced'

My template defaulted to:
* Model: Realistic Vision 4.0
* Prompt Guidance: 7
* Image Dimensions: Instagram Post
* Number of Images: 1

Prompt Guidance caps at 30, and supposedly influences how much the generated content conforms to the prompt. Low default prompt guidance is likely the cause of the strange images generated in the first 5 image prompts. 

Additionally I tried using the following filter:
* Filter: Close-Up Details

## Image Prompts
*Default prompt*:
* “8k close up portrait of a fitness enthusiast engaged in a workout routine, demonstrating strength, agility, and determination, inspiring a healthy and active lifestyle, high resolution, highly detailed”

*Image Prompt #1*:
For the first prompt I simply added "using a fitness tracker".
* "8k close up portrait of a fitness enthusiast engaged in a workout routine, demonstrating strength, agility, and determination, inspiring a healthy and active lifestyle, using a fitness tracker, high resolution, highly detailed and Use a 'Close-up Details' filter to focus on intricate elements, revealing the beauty in small things."
>![prompt output with an extra leg](./images/playgroundAI/Picture1.png)

There is no fitness tracker visible in this image. At first I thought that perhaps "fitness tracker" was not a recognizable prompt, so next I tried "smartwatch" instead.

*Image Prompt #2*:
* "8k close up portrait of a fitness enthusiast engaged in a workout routine, demonstrating strength, agility, and determination, inspiring a healthy and active lifestyle, looking at a smartwatch, high resolution, highly detailed and Use a 'Close-up Details' filter to focus on intricate elements, revealing the beauty in small things."
>![prompt output with an extra arm](./images/playgroundAI/Picture2.png)

There is neither a fitness tracker nor a smartwatch visible in this image. At this point I simplify the prompt by removing "engaged in a workout routine" to see if it improves results.

*Image Prompt #3*:
* "8k close up portrait of a fitness enthusiast, demonstrating strength, agility, and determination, inspiring a healthy and active lifestyle, wearing a smartwatch, high resolution, highly detailed and Use a 'Close-up Details' filter to focus on intricate elements, revealing the beauty in small things."
>![prompt output with an extra hand](./images/playgroundAI/Picture3.png)

There is finally a fitness tracker / smartwatch visible, but the layout of the image with how the arms are positioned is quite nonsensical. I try putting "engaged in a workout routine" back in to see if it fixes the output.

*Image Prompt #4*:
* 8k close up portrait of a fitness enthusiast engaged in a workout routine, demonstrating strength, agility, and determination, inspiring a healthy and active lifestyle, wearing a smartwatch, high resolution, highly detailed and Use a 'Close-up Details' filter to focus on intricate elements, revealing the beauty in small things.
>![prompt output with an extra hand](./images/playgroundAI/Picture4.png)

At this point I am starting to believe that the “wearing a smartwatch” prompt is generating the strange output.

Maybe a simple prompt is better? I am going back to the tried and true “happy person wearing a smartwatch.”

*Image Prompt #5*:
* Happy person wearing a smartwatch
>![prompt output with an extra hand](./images/playgroundAI/Picture5.png)

This output seems relatively normal compared to the last two but the hands are still strange. I am now thinking that Stable Diffusion cannot generate proper hands without negative prompts.

I go back to the Advanced Settings and change some settings in an attempt to fix the output. Additionally, I revise my prompt to "athlete" to have a fitness context but also not too specific.
* Prompt Guidance: 7 --> 30
* Filter: Close-Up Details --> No Filter

*Image Prompt #6*:
* Happy athlete wearing a smartwatch
>![prompt output with an extra hand](./images/playgroundAI/Picture6.png)

This output is much more satisfactory than the rest, possibly because of high prompt guidance. The hand is still slightly strange, as the person is wearing a watch but also holding a watch with some appendages sticking to it.

However, at this point I have used the rest of my prompts for text generation so there will be no more testing until the free prompts are reset in a month.

## Text Prompts
Playground AI has access to multiple text generating models, such as *Chat GPT-3.5*, *Chat GPT-4*, *Ai21*, and *Cohere*.

### *Chat GPT-4*

We have limited prompts left so let's start with Chat GPT-4, supposedly an improvement over Chat GPT-3.5. 

We'll use a similar prompt from our Round 1 testing with CopyAI.

*Text Prompt #1*:
* “Write me a short paragraph explaining how fitness trackers are an important service innovation, including benefits and challenges.”
> Hello! Fitness trackers, as a service innovation, have revolutionized the way we monitor our health and fitness. They provide real-time data on various aspects of our physical activities, such as steps taken, calories burned, heart rate, and sleep patterns. This immediate feedback can motivate individuals to lead healthier lifestyles and achieve their fitness goals. Moreover, the data collected can be used by healthcare professionals to monitor patients' health remotely, thus enhancing healthcare delivery. However, there are challenges associated with fitness trackers. Privacy and data security are major concerns, as sensitive health data can be misused if not properly protected. Additionally, the accuracy of the data collected by these devices can sometimes be questionable, which can lead to misinformation and misinterpretation of one's health status.

The “Hello” is a bit goofy, but it would work for a video script. It is possible that the greeting is because this is my first prompt. In terms of the script, would be better to end on a positive note. Maybe I will include “end on a positive note.”

*Text Prompt #2*:
* Write me a short paragraph explaining how fitness trackers are an important service innovation, including benefits and challenges. End on a positive note.
>Fitness trackers, as a service innovation, have significantly transformed our approach to health and wellness. They offer numerous benefits such as real-time monitoring of vital signs, tracking physical activity, and providing personalized health insights. These devices encourage users to lead healthier lifestyles by setting and achieving fitness goals. However, they also present challenges, including concerns about data privacy and accuracy of the information provided. Despite these challenges, the overall impact of fitness trackers is overwhelmingly positive. They have democratized health information, making it accessible to everyone, and have the potential to significantly improve public health outcomes.

This one is better since it tries to pivots back to a positive impact of the service innovation. I’ll settle with this output for Chat GPT-4.

### *Cohere*
I tried the same prompt for Ai21 but received no response. Instead, we will use our last text prompt on Cohere.

*Text Prompt #1*:
* Write me a short paragraph explaining how fitness trackers are an important service innovation, including benefits and challenges. End on a positive note.
>Service innovations are innovations that are meant to improve the quality of human lives, hopefully in a sustainable manner. 
Fitness trackers are wearable technology that measures various health statistics and fitness-related metrics, such as heart rate, steps taken, and sleep quality. 
An example of the benefit of these devices is that they generate actionable insights and data to help users get healthier: providing motivating challenges, giving users practical tips, or even medically accurate insights to users so they can make healthier choices and potentially even detect irregular health trends or issues before they worsen. 
On the other hand, an example of a challenge of these devices is that the perception of them being reliable as a medical device may lead to over-reliance, acting as a false substitute for actual medical advice, and therefore not act as a solution but instead add to the problem. 
Overall, fitness trackers do seem to offer an important service innovation as long as they are used as a supplement to healthy living and not a replacement. 

The tone for this output seems a bit robotic in how it specifically answers the prompt by providing exactly the words used, like “benefit” and “challenge." Another critique is that contrary to the name, the output for the "challenge" section could be more coherent in wording.

## Ethics Rating: 3/5
| Principle                     | Rating (1-5) | Reasoning                                                                                                                                               |
|-------------------------------|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| **1. Fairness**               |              |                                                                                                                                                         |
| Diverse Representative Data   | 5            | The tool utilizes multiple LLMs and Image Models (Stable Diffusion, OpenJourney, RealisticVision 4.0, etc.) to diversify potential generated responses. |
| Bias Awareness and Mitigation | 2            | The tool does not appear to have any particular measures for bias mitigation in image output. Depicted athletes were primarily light-skinned females.   |
| **2. Reliability**            |              |                                                                                                                                                         |
| Quality Results over Time     | 2            | The tool has notified users that the image generation tool is under maintenance with no specified length.                                               |
| **3. Traceability**           |              |                                                                                                                                                         |
| Source Attribution            | 5            | All text and image models utilized are named, such as ChatGPT and Hugging Face.                                                                         |
| **4. Transparency**           |              |                                                                                                                                                         |
| Resource Accessibility        | 2            | Important features such as Prompt Guidance and Model are hidden under "Advanced" mode and called "rarely used parameters."                              |
| **5. Privacy and Security**   |              |                                                                                                                                                         |
| Third-Party Disclosure        | 3            | The tool pledges to keep user information entered into the chatbot confidential.                                                                        |

## Overall Rating: 1/5

Although there is a somewhat involved tutorial, *PlaygroundAI* fails to sufficiently introduce one of the most important settings to the user: **Prompt Guidance**. As such, many free prompts were used before somewhat satisfactory output was generated. 

### Image Generation: 3/5
The tool fails to deliver realistic flexbility when provided custom prompts even though it shows capability with the example prompts. There is potential with further prompt refinement, but the 10 prompt limit across both image and text generation highly restricts further testing with different image models. 

### Text Generation: 5/5
The tool offers access to multiple services which is a plus. 
* *Chat GPT-4* **(rating: 5/5)** performs respectably
* *Cohere* **(rating: 3/5)** is still catching up to the market

















