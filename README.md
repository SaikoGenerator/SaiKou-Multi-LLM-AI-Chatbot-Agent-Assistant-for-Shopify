# SaiKou - Multi-LLM AI Chatbot Agent/Assistant for Shopify

**SaiKou (最高)**: Japanese for *The Highest, The Best, Supreme*.

SaiKou is an open-source, multi-LLM AI chat agent for Shopify. It provides a powerful, customizable chat widget that integrates seamlessly with your storefront, allowing you to connect with customers, boost sales, and provide instant support using the AI provider of your choice.

---

## ✨ Key Features

- **🤖 Multi-LLM Support**: Natively supports major AI providers including **Claude, OpenAI, Google Gemini, Groq, and OpenRouter**. Switch between them with ease.
- **⚙️ Simple Configuration**: A user-friendly admin dashboard in your Shopify store to select your AI provider and enter API keys securely. No coding required.
- **🔒 Secure**: API keys are fully encrypted (AES-256-GCM) when stored in the database.
- **🛍️ Deep Shopify Integration**: Uses the Model Context Protocol (MCP) to interact with Shopify APIs. The agent can:
    - Search the product catalog.
    - Add/remove items from the cart.
    - Initiate checkout.
    - Look up store policies and FAQs.
    - Check order status.
- **🎨 Customizable UI**: The chat widget's appearance can be customized with CSS to match your brand.
- **🚀 Built for Developers**: Built on a modern stack (Remix, React, Prisma) and designed to be easily extensible.

---

## 🚀 Getting Started

Follow these steps to get the SaiKou agent running on your development store.

### Prerequisites

- A Shopify Partner account and a development store.
- [Node.js](https://nodejs.org/en/) (version 18.20 or higher).
- The [Shopify CLI](https://shopify.dev/docs/apps/tools/cli).

### Installation & Setup

1.  **Clone the repository:**
    ```bash
    git clone <repository-url>
    cd SaiKou-Multi-LLM-AI-Chatbot-Agent-Assistant-for-Shopify
    ```

2.  **Install dependencies:**
    ```bash
    npm install
    ```

3.  **Connect to your Shopify store:**
    The Shopify CLI will prompt you to log in and select your organization and store.
    ```bash
    npm run config:link
    ```

4.  **Create your environment file:**
    Copy the example environment file.
    ```bash
    cp .env.example .env
    ```
    You will need to fill in the `SHOPIFY_API_KEY` and `SHOPIFY_API_SECRET` which are provided after running `npm run config:link`. You also need to ensure the `ENCRYPTION_KEY` is set. The other keys can be left blank as we will configure them in the admin UI.

5.  **Run the development server:**
    ```bash
    npm run dev
    ```
    This will start the app and provide you with a URL to install it on your development store. Open the URL and follow the prompts to install the app.

---

## 🔧 Configuration

Once the app is installed, you can configure your AI provider through the admin dashboard:

1.  In your Shopify Admin, go to **Apps** and open the **SaiKou Chatbot** app.
2.  Navigate to the **Settings** page using the top navigation menu.
3.  From the dropdown, select your desired **LLM Provider** (e.g., Gemini).
4.  Enter your **API Key** for that provider in the password field.
5.  Click **Save**.

The chat agent on your storefront will now be powered by your selected provider!

*Note: The app can also be configured using environment variables as a fallback. See the `.env.example` file for more details.*

---

## 🤝 Contributing

Contributions are welcome! This project is open-source and we encourage you to help us make it even better.

To contribute:
1.  Fork the repository.
2.  Create a new branch for your feature (`git checkout -b feature/AmazingFeature`).
3.  Commit your changes (`git commit -m 'Add some AmazingFeature'`).
4.  Push to the branch (`git push origin feature/AmazingFeature`).
5.  Open a Pull Request.

Please make sure your code follows the project's coding standards.

---

## 📄 License

This project is licensed under the MIT License. See the `LICENSE.md` file for details.
