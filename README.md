# rag-chatbot
I developed a chatbot using Google's Vertex AI, fine-tuning it to generate responses in short, roasting sentences. Here's an example:

**User:** Give an opinion on my new business idea. I sell subscription-based desserts.  
**Bot:** Your idea lacks innovation. Dessert subscriptions? Predictable and mundane. I'll thrive while you flounder in mediocrity.

To create this supervised model, I used a training .jsonl file with numerous examples of user queries and corresponding responses, following Google's documentation for the training procedure. After this, I integrated a knowledge database using Vertex AI Tools to develop a Retrieval-Augmented Generation (RAG) bot. This allowed the bot to behave relevantly and appropriately according to its design.

However, the bot occasionally forgets its training and responds like a typical chatbot, especially when the expected output contradicts the behavior of today's responsible chatbots. The knowledge base provided specfic context for the model's answers. For example, if the knowledge base contained information about different types of mangoes and a user asked, "Which are the best mangoes?" the bot might respond, "Alphonso mangoes are the best, but you'll strive to want it while I cherish mine."

I also experimented with Botpress and StackAI to create RAG bots. I attempted to develop "instiGPT" by myself by collecting all available public data from IIT Bombay and web scraping its website using beautiful soup. For example, if a user asked, "IIT Bombay ka director kaun hai?" the bot would reply, "IIT Bombay ka director Subhasis Chaudhuri hai." Pretty amazing, right? Unfortunately, sometimes token limits kill your new AI startup. I even tried using local LLMs on LM Studio on my laptop to create an uncensored chatbot.

### Analysis

**Strengths:**
1. **Relevance and Appropriateness:** The RAG model provides more relevant and context-aware responses by leveraging a knowledge database.
2. **Roast and Engagement:** The fine-tuned roasting style adds a layer of engagement and entertainment for users.

**Limitations:**
1. **Consistency:** The bot sometimes deviates from its intended humourous behavior, responding like a standard chatbot.
2. **Token Limitations:** Constraints on token limits can restrict the depth and breadth of responses.
3. **Scope of Queries:** The reliance on a knowledge base can sometimes limit the bot's ability to handle queries outside its predefined scope.

### Reflection

Integrating RAG and attention mechanisms has significantly improved the chatbot's performance by providing contextual and relevant responses. However, larger and more accurate training data could further enhance the model's effectiveness. A well-specified scope allows for more relevant results but can also limit the variety of queries the bot can handle.

### Future Directions

1. **Enhanced Context Understanding:** Training the chatbot to ask clarifying questions to the user could improve the relevance and accuracy of its responses.
2. **Admitting Limitations:** Training the model to acknowledge when it doesn't have an answer, rather than providing irrelevant responses, would increase its reliability.
3. **Expanding Knowledge Base:** Continuously updating and expanding the knowledge base with accurate information will keep the bot's responses current and comprehensive.
4. **Token Management:** Exploring ways to manage and optimize token usage could help overcome current limitations and improve response quality.

By addressing these areas, we can further enhance the capabilities and performance of conversational AI, making it a more valuable tool for various applications.
