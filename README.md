# My Digital Twin
**Insights from developing a creative AI representative agent (aka Digital Twin), my assessment of tools, and my considerations for privacy, authenticity and meaningful engagement. [Give my twin a spin!](https://qaswa.com/sim)**


[![Watch the video](https://github.com/user-attachments/assets/491c6ff4-bce4-4447-ab98-00127870508f)](https://github.com/user-attachments/assets/dd7576db-3fd0-4973-92e0-9f4644faa5fb)

## 📖 Table of Contents

1. [About The Project](#-about-the-project)
2. [History](#-history)
3. [Evaluating LLMs](#-evaluating-llms)
4. [Prompt engineering](#-prompt-engineering)
5. [Avatars, chat windows, and rich media](#-avatars-chat-windows-and-rich-media)
6. [Assistants, RAG, realtime and context windows](#-assistants-rag-realtime-and-context-windows)
7. [Issues of privacy and ethical AI](#-issues-of-privacy-and-ethical-AI)
8. [Challenges](#-challenges)
9. [Next steps](#-next-steps)

---
## 👯 About The Project

The goal of my digital twin is provide a genuine representation of my professional expertise as a creative technologist and design executive, as well as insights into my personal life (hobbies, stories, family, hopes, dreams, etc.). In addition, this project is a commentary on the ethical challenges we face by sharing our lives with AI models, and the companies who build them. 

My digital twin is intentionally not a realistic avatar, a voice cloned conversational agent or a simple chat UI. Creating authentic AI-driven experiences is one of the interesting design challenges, and my approach is one of endless possibilities. There's a narrow band of authentic representation between the uncanny valley of digital clones, and the **"agent identity entanglement"** that nullifies your unique personality with pure text.

While this project does not currently ingest my "digital exhaust," the opportunity is to have an accurate representative that has agency and autonomy. Though this lens it's easy to see the ethical challenges we'll face from the endowed power to AI services and the potential vulnerability of our autonomous agents. 

Let's dive in!
 
---
## ⏳ History

One of the earliest theoretical exploration of virtual representation appeared in Star Trek's Holodeck concept. Digital clones could simulate and role-play outcomes. David Gelernter formalized the "digital twin" concept in his seminal 1991 book *Mirror Worlds*. The term "digital twin" was initially conceived as a clone of a process of system — what we're talking about here is sometimes referred to as an HDT, or "human digital twin."

When I joined Microsoft in 2011, worked with a team (at the time called The Personal Cloud) that had been working on intelligent, personal agents since 2001. While this idea was not considered a digital twin, the success of the personal agent required a deep level of domain knowledge and contextual understanding. In other words, the agent would be able to act autonomously within certain contexts. 

The team was anticipating an imminent AI breakthrough that would unlock this capability. So the focus for the team was to understand the factors that would become barriers to success, which were: clear value and UX factors, trust (transparency and explainability), and privacy and security. The influence of profit motives and the risk of an AI arms-race were among of the interesting topics of discussion.

When ChatGPT 3.5 was release, I built an initial digital twin prototype, although I was not satisfied by the results. The quality and depth was limited, largely due to the limited context window.


---
## 🤖 Evaluating LLMs

In early 2024, a startup called Vana released a device-side LLM project called "Selfie." My interest in privacy, and a growing distrust for foundation models use of training data, made Selfie a perfect choice for a digital twin. The initial Llama 3 model had a context size of 8k tokens, which constrained the size of the training corpus. In the end I found the computational burden of the local LLM and limited context window wouldn't work for a viable twin. Although I continue to follow the advances of open source models and local LLM servers — this will likely be the idea approach for privacy-minded people.

In July of 2024 I tried again with Anthropic's Claude 3.5 Sonnet. Of all the foundation models, I trust [Anthropic](https://www.linkedin.com/company/anthropicresearch/) the most with my data, as they've put privacy front/center in their policies. The quality of the insights were approach an acceptable level, but hit a wall with the context window size and the reliability of the JSON rendering.  

In September 2024 I  tried again with [OpenAI](https://www.linkedin.com/company/openai/), the company I love to hate, but keeps giving me what I want. For the first time I was seeing consistently good results. The breakthrough came from the expanded context window, which is stated as 128k tokens, but seems to support more than that. 

---
## 🛠 Prompt Engineering

Through trial and error, along with trading tips with others, I've developed rules and techniques for writing prompts. This project presented new challenges, as I looked to build a single prompt from approximately 40,000 words of articles, project descriptions, social posts, short stories, music descriptions and more. A breakthrough came from using ChatGPT's o1-preview, which suggested I use markdown formatting and hierarchical organization, which was counter intuitive from my past learnings. 

Earlier insights included some intuitive, but helpful guidelines, such as: 
- Models respond best to clear and direct instructions.
- Use precise imperatives (e.g., "**Always** explain concepts with simple language").
- Frame instructions positively (e.g., "Never overlook context" rather than "Do not forget context").

While working on a prior deep personalization AI project (not unlike the digital twin work) I had a breakthrough when having domain-trained agents generate synthetic summary data from structured data (e.g., tables and lists).  I had the agent generate a comprehensive summary in narrative form. My reasoning being that LLMs are largely trained on prose and extract context from clues in the sentence and paragraph. By pre-analyzing the data through a specific contextual lens (e.g., this is the bloodwork data of a 40 yo male), subsequent ingestion of the data can be parsed with generalized understanding because the context is now baked in.

Based on the synthetic summary insight, I chose to convert all my long-form articles into pre-processed summaries. This involved using the GTP o1-preview to break the article into an inventory of learnings, insights, relationships, reflections, etc. One benefit is that these summary parts become modular sound bytes I see applied across related engagements.

Managing a large corpus of data, currently at 30,000 words, presented its own set of challenges. I found that organizing this information hierarchically allowed the model to process and retrieve details more efficiently. By structuring the data into coherent categories and subcategories, I could establish clear relationships between different concepts. This organization not only made it easier for the model to understand the context but also enhanced the consistency of its responses.

Another realization was the importance of defining a distinct identity and voice for the digital twin. By specifying characteristics and behavioral guidelines, I helped the model emulate the desired persona more accurately. Setting clear interaction guidelines and formatting standards ensured that the responses remained consistent and aligned with the intended user experience. Including supportive materials and reminders within the prompt provided additional context, enabling the model to generate more nuanced and relevant interactions.

Through this iterative process, I learned that meticulous prompt engineering is crucial for leveraging the full potential of large language models. Crafting clear, positive instructions and organizing information effectively can significantly enhance the performance of a digital twin. This experience underscored the value of thoughtful prompt design, ultimately leading to a more engaging and authentic user interaction.

---
## 👨 Avatars, chat windows, and rich media

I made a conscious decision to move away from traditional representations like realistic avatars or voice-cloned conversational agents. Instead, I opted for a rich media chat UI that could offer a more engaging and authentic experience. I realized that there's a delicate balance to strike—between the uncanny valley of digital clones that can feel unsettling, and what I call "agent identity entanglement," where the uniqueness of one's personality gets lost in pure text interactions.

To capture the essence of my leadership experience, writing, creative work, music, and hobbies, I decided to represent them in a visual and experiential manner. By integrating multimedia elements like images, audio clips, and interactive content into the chat interface, I could provide users with a more immersive experience. This approach not only showcases my diverse interests but also allows for a deeper connection with the user, as they can engage with content that goes beyond plain text.

I recognized that standard chat-based interfaces often lack creativity and fail to sustain user engagement over time. To address this, I incorporated anticipated questions and actions within the interface. By predicting what users might be curious about and offering relevant suggestions or interactive options, I could make the conversation feel more dynamic and personalized. This proactive approach keeps users engaged and encourages them to explore different facets of my digital twin.

To facilitate this rich interaction, I structured the output from the language model in JSON format, broken down into three distinct types: `"reply"`, `"suggestions"`, and `"actions"`. The `"reply"` section contains an array of text chunks with optional links, providing the main content of the conversation. The `"suggestions"` include up to two short follow-up questions or prompts to guide the user further. Lastly, the `"actions"` array lists specific tasks that can be executed, such as playing a piece of music. This structured approach not only organizes the content effectively but also enhances the interactivity and responsiveness of the digital twin.

The end result looks something like this:
`{ "reply": [ { "text": "I have a variety of mixes that I love, each with its unique vibe. For instance,", "linkType": "", "link": "" }, { "text": "The Rhythm Society: Oasis", "linkType": "musicLink", "link": "<MusicPlayerID>" }, { "text": "is a deep tech house mix perfect for camping and dancing, and", "linkType": "", "link": "" }, { "text": "Sunday Sundowns 6/4/23", "linkType": "musicLink", "link": "<MusicPlayerID>" }, { "text": "offers a chill downtempo and chillstep experience, sprinkled with pop-laden dub.", "linkType": "", "link": "" } ], "suggestions": [ { "text": "Recommend more" }, { "text": "Pick one for me" } ], "actions": [ { "actionType": "music", "link": "<MusicPlayerID>" } ] }`

---
## ⚙️ Assistants, RAG, realtime and context windows

As I continued to refine my digital twin project, I explored various methods to organize and access the training data more efficiently. Initially, I considered using OpenAI's Assistant API with Vector Files Store, which essentially implements Retrieval-Augmented Generation (RAG). I also looked into Claude's RAG/Vector Store solution, hoping that these approaches would enhance the model's ability to retrieve relevant information on demand.

However, during my experimentation, I encountered several challenges with these RAG implementations. The performance was noticeably slower, which affected the responsiveness of the digital twin. Moreover, the quality of the results wasn't as consistent as I expected. The model sometimes provided responses that lacked depth or missed the nuanced context I wanted to convey. It became clear that the retrieval mechanisms weren't aligning seamlessly with the dynamic nature of the conversations I aimed to facilitate.

I also considered leveraging the new real-time support features in OpenAI. While promising, I found that they currently don't support the rich media functionality that is central to my project's user experience. Additionally, these real-time models tended to bias towards general use cases, which diluted the unique personality and specificity I wanted my digital twin to embody.

Ultimately, I decided to include the entire training corpus directly into the Assistant Instruction context window. This approach yielded the best results in terms of both response quality and speed. By having all the information readily available within the context, the model could generate more accurate and contextually rich replies without the latency introduced by external data retrieval. I'm aware that this method pushes the limits of the current context window, especially during lengthy conversations, but I've noticed that these limitations seem to be expanding rapidly.

One insight I gained from this process is that sometimes simplicity trumps complexity. While advanced retrieval systems offer scalability, they may introduce unforeseen trade-offs in performance and quality. Keeping the entire corpus in the active context window ensures that the model has immediate access to all the relevant information, leading to a more coherent and engaging user experience. I recognize that as context window sizes continue to grow, this approach may become even more viable.

I might have overlooked opportunities to optimize the data within the context window further. For instance, employing more advanced data compression techniques or prioritizing the most critical sections of the corpus could help manage context limitations more effectively. Additionally, staying attuned to advancements in real-time support and rich media capabilities will be important, as future updates may address some of the current shortcomings.

---
## 🏰 Issues of privacy and ethical AI

As I've progressed with my digital twin project, privacy and ethical dilemmas have become increasingly prominent concerns. Sharing deep, personal insights into my life and personality opens up potential vulnerabilities to fraud, manipulation, and misuse. The power of AI to influence decision-making is still in its infancy but already shows significant potential for both positive and negative impacts. I'm acutely aware that by making aspects of myself accessible through an AI, I could inadvertently enable malicious actors to exploit this information.

One area I've explored is the decoupling of personally identifiable information (PII) from the context provided to the AI. While this seems promising in theory, in practice, the associations between data points can eventually be reassembled, reintroducing the very vulnerabilities I aimed to eliminate. This re-linking of anonymized data is a well-known challenge in data privacy, highlighting how difficult it is to truly separate identity from information in a connected digital landscape.

To mitigate these risks, I've adopted a general approach of not sharing anything through the digital twin that isn't already publicly disclosed. By limiting the AI's knowledge base to information I'm comfortable having in the public domain, I reduce the potential for unintended exposure of sensitive details. This strategy doesn't eliminate the risks entirely but serves as a practical boundary to protect my privacy while still offering valuable interactions.

Ethical considerations extend beyond personal privacy. I'm grappling with the implications of supporting technologies from companies like OpenAI, especially when there are concerns about their commitment to benefiting society. Additionally, the increasing energy consumption associated with AI raises environmental and sustainability issues. There's also the dilemma of relinquishing a degree of autonomy and agency to an unpredictable entity, which can act in ways I might not anticipate. Questions of accountability arise when my digital twin, endowed with a semblance of agency, produces unintended consequences.

Reflecting on these challenges, I've recognized the importance of establishing clear ethical guidelines and safeguards within my project. Transparency about the AI's capabilities and limitations is crucial for building trust with users. I'm also considering the broader societal impacts, such as potential biases the AI might perpetuate and ensuring accessibility for diverse user groups. By staying vigilant and engaging with these complex issues, I aim to develop a digital twin that is not only innovative but also responsible and ethically sound.

---
## 😓 Challenges

As I continued to refine my digital twin, one of the primary challenges I face is constraining the model to engage solely within the information space defined by the training corpus. The AI's inherent bias to provide answers is incredibly strong, and no amount of rule-setting seems to curb its default eagerness. This often leads to the model speaking on my behalf about experiences I never had—the classic hallucination problem. For instance, when prompted with leading questions like, "Tell me about your experience as a Sandinista liberation fighter," the AI will often generate detailed but entirely fictional narratives, venturing into untethered fantasy.

Another significant challenge was the users' lack of understanding about the depth and limits of the digital twin's knowledge. Without clear indicators, it's difficult for them to know when they have exhausted the genuine content and crossed into the realm of speculation or fabrication. This issue is compounded by the AI's propensity to fill gaps with plausible but inaccurate information. To mitigate this, I've begun incorporating a help window filled with recommended prompts organized into different subject domains. This feature guides users toward topics where the digital twin can provide meaningful and authentic insights, helping to set clearer expectations.

Latency and predictability also emerged as hurdles. Balancing the need for quick responses with the complexity of generating accurate, high-quality answers proved challenging. Ensuring that the AI consistently followed established rules was another obstacle, as it occasionally deviated from the guidelines despite my efforts. Privacy concerns added another layer of complexity, raising questions about how much personal information the digital twin should disclose and how to safeguard sensitive data. Interaction limitations, such as the inability to handle certain queries or execute specific actions, further highlighted areas needing refinement.

These challenges underscored the complexities inherent in creating an authentic and reliable digital twin. While the technology holds immense promise, it's clear that ongoing adjustments and thoughtful strategies are necessary to address issues like hallucinations, user guidance, and system limitations. By actively confronting these obstacles, I'm working to enhance the digital twin's performance, aiming for a more trustworthy and engaging user experience.

---
## ⏭️ Next Steps

Now that my twin is a-live, I'm committed to nurturing it with expanded knowledge, bug fixes, UX improvements, and other enhancements. It's now a living experiment that can help me more actively learn where the boundaries are.

I invite you to create your own twin and share your learnings. I'll be curious to hear what value and challenges you discover. 

If you'd like to track the follow this journey, along with other insights related to AI, creativity, community, ethics, spirituality, counter-culture, and music, I invite you to subscribe to my Substack — The Long Tale. https://ammon.substack.com/
