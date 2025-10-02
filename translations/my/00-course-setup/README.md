<!--
CO_OP_TRANSLATOR_METADATA:
{
  "original_hash": "9b03446058b4eed46928ae5e46325ea0",
  "translation_date": "2025-10-02T19:24:53+00:00",
  "source_file": "00-course-setup/README.md",
  "language_code": "my"
}
-->
# သင်ခန်းစာ စတင်ခြင်း

## မိတ်ဆက်

ဒီသင်ခန်းစာမှာ ဒီသင်တန်းရဲ့ ကုဒ်နမူနာတွေကို ဘယ်လို run လုပ်မလဲဆိုတာကို ဖော်ပြပေးမှာပါ။

## အခြား သင်ယူသူတွေနဲ့ ပေါင်းသင်းပြီး အကူအညီရယူပါ

သင့် repo ကို clone လုပ်ဖို့မစတင်ခင် [AI Agents For Beginners Discord channel](https://aka.ms/ai-agents/discord) ကို join လုပ်ပါ။ ဒီမှာ setup အတွက် အကူအညီရယူနိုင်သလို၊ သင်တန်းနဲ့ပတ်သက်တဲ့ မေးခွန်းတွေမေးနိုင်ပါတယ်။ အခြား သင်ယူသူတွေနဲ့လည်း ဆက်သွယ်နိုင်ပါတယ်။

## ဒီ Repo ကို Clone လုပ်ပါ သို့မဟုတ် Fork လုပ်ပါ

စတင်ဖို့အတွက် GitHub Repository ကို clone သို့မဟုတ် fork လုပ်ပါ။ ဒါက သင့်ကိုယ်ပိုင် သင်တန်းစာအုပ်ကို ရရှိစေပြီး ကုဒ်တွေကို run, test, tweak လုပ်နိုင်ပါမယ်။

<a href="https://github.com/microsoft/ai-agents-for-beginners/fork" target="_blank">repo ကို fork လုပ်ရန်</a> link ကို နှိပ်ပါ။

အခု သင့်မှာ ဒီသင်တန်းရဲ့ fork လုပ်ထားတဲ့ ကိုယ်ပိုင် version ရရှိထားပါပြီ။

![Forked Repo](../../../translated_images/forked-repo.33f27ca1901baa6a5e13ec3eb1f0ddd3a44d936d91cc8cfb19bfdb9688bd2c3d.my.png)

## ကုဒ်ကို Run လုပ်ခြင်း

ဒီသင်တန်းမှာ AI Agents တည်ဆောက်ဖို့ လက်တွေ့အတွေ့အကြုံရရှိစေမယ့် Jupyter Notebooks တွေပါဝင်ပါတယ်။

ကုဒ်နမူနာတွေမှာ အောက်ပါ framework တွေကို အသုံးပြုထားပါတယ်-

**GitHub Account လိုအပ်သည် - အခမဲ့**:

1) Semantic Kernel Agent Framework + GitHub Models Marketplace (semantic-kernel.ipynb)
2) AutoGen Framework + GitHub Models Marketplace (autogen.ipynb)

**Azure Subscription လိုအပ်သည်**:
3) Azure AI Foundry + Azure AI Agent Service (azureaiagent.ipynb)

သုံးမျိုးလုံးကို စမ်းသုံးဖို့ အကြံပေးပါတယ်။ သင့်အတွက် အကောင်းဆုံးဖြစ်မယ့် နမူနာကို ရွေးချယ်နိုင်ပါမယ်။

သင်ရွေးချယ်တဲ့ option အပေါ်မူတည်ပြီး အောက်မှာ ဖော်ပြထားတဲ့ setup အဆင့်တွေကို လိုက်နာရပါမယ်။

## လိုအပ်ချက်များ

- Python 3.12+
  - **NOTE**: Python3.12 မရှိပါက Python3.12 ကို install လုပ်ပါ။ requirements.txt ဖိုင်ထဲက version တွေကို install လုပ်ဖို့ python3.12 ကို အသုံးပြုပြီး venv တည်ဆောက်ပါ။

    >ဥပမာ

    Python venv directory တည်ဆောက်ခြင်း:

    ``` bash
    python3 -m venv venv
    ```

    venv environment ကို activate လုပ်ရန်:

    macOS နှင့် Linux

    ```bash
    source venv/bin/activate
    ```
  
    Windows

    ```bash
    venv\Scripts\activate
    ```

- GitHub Account - GitHub Models Marketplace ကို အသုံးပြုရန်
- Azure Subscription - Azure AI Foundry ကို အသုံးပြုရန်
- Azure AI Foundry Account - Azure AI Agent Service ကို အသုံးပြုရန်

ဒီ repository ရဲ့ root မှာ `requirements.txt` ဖိုင်ကို ထည့်ထားပြီး Python packages တွေကို install လုပ်ဖို့လိုအပ်ပါတယ်။

Terminal မှာ အောက်ပါ command ကို run လုပ်ပြီး install လုပ်နိုင်ပါတယ်:

```bash
pip install -r requirements.txt
```
Python virtual environment တည်ဆောက်ဖို့ အကြံပေးပါတယ်။ conflicts နဲ့ ပြဿနာတွေကို ရှောင်ရှားနိုင်ပါတယ်။

## VSCode Setup
VSCode မှာ Python ရဲ့ မှန်ကန်တဲ့ version ကို အသုံးပြုနေကြောင်း သေချာပါစေ။

![image](https://github.com/user-attachments/assets/a85e776c-2edb-4331-ae5b-6bfdfb98ee0e)

## GitHub Models ကို အသုံးပြုတဲ့ နမူနာများအတွက် Setup

### အဆင့် ၁: GitHub Personal Access Token (PAT) ကို ရယူပါ

ဒီသင်တန်းမှာ GitHub Models Marketplace ကို အသုံးပြုထားပြီး Large Language Models (LLMs) တွေကို အခမဲ့ access ရရှိစေပါတယ်။

GitHub Models ကို အသုံးပြုဖို့ [GitHub Personal Access Token](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/managing-your-personal-access-tokens) တစ်ခုကို ဖန်တီးဖို့လိုအပ်ပါတယ်။

GitHub Account ရဲ့ <a href="https://github.com/settings/personal-access-tokens" target="_blank">Personal Access Tokens settings</a> ကို သွားပါ။

Token ဖန်တီးတဲ့အခါ [Principle of Least Privilege](https://docs.github.com/en/get-started/learning-to-code/storing-your-secrets-safely) ကို လိုက်နာပါ။ Token ကို ဒီသင်တန်းရဲ့ ကုဒ်နမူနာတွေကို run လုပ်ဖို့လိုအပ်တဲ့ permission တွေကိုပဲ ပေးပါ။

1. **Developer settings** မှာ `Fine-grained tokens` option ကို ရွေးပါ။
   ![](../../../translated_images/profile_developer_settings.410a859fe749c755c859d414294c5908e307222b2c61819c3203bbeed4470e25.my.png)

    ပြီးရင် `Generate new token` ကို ရွေးပါ။

    ![Generate Token](../../../translated_images/fga_new_token.1c1a234afe202ab37483944a291ee80c1868e1e78082fd6bd4180fea5d5a15b4.my.png)

2. Token ရဲ့ ရည်ရွယ်ချက်ကို ဖော်ပြတဲ့ နာမည်တစ်ခုကို ထည့်ပါ။

    🔐 Token Duration အကြံပေးချက်

    အကြံပေးထားတဲ့ သက်တမ်း: 30 ရက်  
    ပိုမိုလုံခြုံတဲ့အနေအထားအတွက် 7 ရက်လိုမျိုး ပိုတိုတဲ့ သက်တမ်းကို ရွေးချယ်နိုင်ပါတယ် 🛡️  
    သင်တန်းကို အချိန်မကုန်အောင် ပြီးမြောက်ဖို့ သင့်ကိုယ်ပိုင် ရည်မှန်းချက်တစ်ခုထားနိုင်ပါတယ် 🚀။

    ![Token Name and Expiration](../../../translated_images/token-name-expiry-date.a095fb0de63868640a4c82d6b1bbc92b482930a663917a5983a3c7cd1ef86b77.my.png)

3. Token ရဲ့ scope ကို ဒီ repository ရဲ့ fork အတွက်သာ ကန့်သတ်ပါ။

    ![Limit scope to fork repository](../../../translated_images/token_repository_limit.924ade5e11d9d8bb6cd21293987e4579dea860e2ba66d607fb46e49524d53644.my.png)

4. Token ရဲ့ permissions ကို ကန့်သတ်ပါ: **Permissions** အောက်မှာ **Account** tab ကို နှိပ်ပြီး "+ Add permissions" button ကို နှိပ်ပါ။ Dropdown menu မှာ **Models** ကို ရှာပြီး checkbox ကို အမှန်ခြစ်ပါ။
    ![Add Models Permission](../../../translated_images/add_models_permissions.c0c44ed8b40fc143dc87792da9097d715b7de938354e8f771d65416ecc7816b8.my.png)

5. Token ဖန်တီးမည့်အခါ လိုအပ်တဲ့ permissions တွေကို စစ်ဆေးပါ။ ![Verify Permissions](../../../translated_images/verify_permissions.06bd9e43987a8b219f171bbcf519e45ababae35b844f5e9757e10afcb619b936.my.png)

6. Token ကို ဖန်တီးမည့်အခါ password manager vault လိုမျိုး လုံခြုံတဲ့နေရာမှာ သိမ်းဆည်းထားဖို့ သေချာပါ။ Token ကို ဖန်တီးပြီးနောက် ပြန်လည်ကြည့်ရှုနိုင်မည်မဟုတ်ပါ။ ![Store Token Securely](../../../translated_images/store_token_securely.08ee2274c6ad6caf3482f1cd1bad7ca3fdca1ce737bc485bfa6499c84297c789.my.png)

ဖန်တီးထားတဲ့ token ကို copy လုပ်ပါ။ အခု သင့် `.env` ဖိုင်ထဲမှာ ထည့်သွင်းပါ။

### အဆင့် ၂: `.env` ဖိုင်ကို ဖန်တီးပါ

Terminal မှာ အောက်ပါ command ကို run လုပ်ပါ။

```bash
cp .env.example .env
```

ဒီ command က `.env` ဖိုင်ကို သင့် directory မှာ ဖန်တီးပြီး environment variables တွေကို ထည့်သွင်းနိုင်မယ့်နေရာကို ဖန်တီးပေးပါမယ်။

Token ကို copy လုပ်ပြီး `.env` ဖိုင်ကို သင့်အကြိုက်ဆုံး text editor မှာ ဖွင့်ပါ။ `GITHUB_TOKEN` field ထဲမှာ token ကို paste လုပ်ပါ။
![GitHub Token Field](../../../translated_images/github_token_field.20491ed3224b5f4ab24d10ced7a68c4aba2948fe8999cfc8675edaa16f5e5681.my.png)

အခု သင့်မှာ ဒီသင်တန်းရဲ့ ကုဒ်နမူနာတွေကို run လုပ်နိုင်ပါပြီ။

## Azure AI Foundry နဲ့ Azure AI Agent Service ကို အသုံးပြုတဲ့ နမူနာများအတွက် Setup

### အဆင့် ၁: Azure Project Endpoint ကို ရယူပါ

Azure AI Foundry မှ hub နဲ့ project တစ်ခုကို ဖန်တီးဖို့အဆင့်တွေကို [Hub resources overview](https://learn.microsoft.com/en-us/azure/ai-foundry/concepts/ai-resources) မှာ ကြည့်ရှုပါ။

Project ကို ဖန်တီးပြီးနောက် connection string ကို ရယူဖို့လိုအပ်ပါတယ်။

ဒီအရာကို Azure AI Foundry portal ရဲ့ **Overview** စာမျက်နှာမှာ ပြုလုပ်နိုင်ပါတယ်။

![Project Connection String](../../../translated_images/project-endpoint.8cf04c9975bbfbf18f6447a599550edb052e52264fb7124d04a12e6175e330a5.my.png)

### အဆင့် ၂: `.env` ဖိုင်ကို ဖန်တီးပါ

Terminal မှာ အောက်ပါ command ကို run လုပ်ပါ။

```bash
cp .env.example .env
```

ဒီ command က `.env` ဖိုင်ကို သင့် directory မှာ ဖန်တီးပြီး environment variables တွေကို ထည့်သွင်းနိုင်မယ့်နေရာကို ဖန်တီးပေးပါမယ်။

Token ကို copy လုပ်ပြီး `.env` ဖိုင်ကို သင့်အကြိုက်ဆုံး text editor မှာ ဖွင့်ပါ။ `PROJECT_ENDPOINT` field ထဲမှာ token ကို paste လုပ်ပါ။

### အဆင့် ၃: Azure ကို Sign in လုပ်ပါ

လုံခြုံရေးအတွက် [keyless authentication](https://learn.microsoft.com/azure/developer/ai/keyless-connections?tabs=csharp%2Cazure-cli?WT.mc_id=academic-105485-koreyst) ကို အသုံးပြုပါ။

Terminal ကို ဖွင့်ပြီး `az login --use-device-code` command ကို run လုပ်ပါ။ Azure account ကို sign in လုပ်ပါ။

Sign in လုပ်ပြီးနောက် terminal မှာ subscription ကို ရွေးချယ်ပါ။

## အပိုသော Environment Variables - Azure Search နဲ့ Azure OpenAI

Agentic RAG Lesson - Lesson 5 - မှာ Azure Search နဲ့ Azure OpenAI ကို အသုံးပြုတဲ့ နမူနာတွေပါဝင်ပါတယ်။

ဒီနမူနာတွေကို run လုပ်ချင်ရင် `.env` ဖိုင်ထဲမှာ အောက်ပါ environment variables တွေကို ထည့်သွင်းဖို့လိုအပ်ပါတယ်:

### Overview Page (Project)

- `AZURE_SUBSCRIPTION_ID` - **Overview** စာမျက်နှာရဲ့ **Project details** မှာ ရှာပါ။

- `AZURE_AI_PROJECT_NAME` - **Overview** စာမျက်နှာရဲ့ အပေါ်မှာ project နာမည်ကို ကြည့်ပါ။

- `AZURE_OPENAI_SERVICE` - **Overview** စာမျက်နှာရဲ့ **Included capabilities** tab မှာ **Azure OpenAI Service** ကို ရှာပါ။

### Management Center

- `AZURE_OPENAI_RESOURCE_GROUP` - **Management Center** ရဲ့ **Overview** စာမျက်နှာမှာ **Project properties** ကို သွားပါ။

- `GLOBAL_LLM_SERVICE` - **Connected resources** အောက်မှာ **Azure AI Services** connection နာမည်ကို ရှာပါ။ မရှိပါက **Azure portal** ရဲ့ resource group မှ AI Services resource နာမည်ကို စစ်ဆေးပါ။

### Models + Endpoints Page

- `AZURE_OPENAI_EMBEDDING_DEPLOYMENT_NAME` - embedding model (ဥပမာ `text-embedding-ada-002`) ကို ရွေးပြီး model details မှ **Deployment name** ကို မှတ်သားပါ။

- `AZURE_OPENAI_CHAT_DEPLOYMENT_NAME` - chat model (ဥပမာ `gpt-4o-mini`) ကို ရွေးပြီး model details မှ **Deployment name** ကို မှတ်သားပါ။

### Azure Portal

- `AZURE_OPENAI_ENDPOINT` - **Azure AI services** ကို ရှာပြီး **Resource Management**, **Keys and Endpoint** ကို သွားပါ။ "Azure OpenAI endpoints" မှ "Language APIs" ကို copy လုပ်ပါ။

- `AZURE_OPENAI_API_KEY` - အတူတူသော screen မှာ KEY 1 သို့မဟုတ် KEY 2 ကို copy လုပ်ပါ။

- `AZURE_SEARCH_SERVICE_ENDPOINT` - **Azure AI Search** resource ကို ရှာပြီး **Overview** ကို ကြည့်ပါ။

- `AZURE_SEARCH_API_KEY` - **Settings** မှာ **Keys** ကို သွားပြီး primary သို့မဟုတ် secondary admin key ကို copy လုပ်ပါ။

### External Webpage

- `AZURE_OPENAI_API_VERSION` - [API version lifecycle](https://learn.microsoft.com/en-us/azure/ai-services/openai/api-version-deprecation#latest-ga-api-release) စာမျက်နှာရဲ့ **Latest GA API release** ကို သွားပါ။

### Keyless Authentication Setup

Credentials တွေကို hardcode မလုပ်ဘဲ Azure OpenAI နဲ့ keyless connection ကို အသုံးပြုပါ။ `DefaultAzureCredential` ကို import လုပ်ပြီး `DefaultAzureCredential` function ကို later call လုပ်ပါ။

```python
from azure.identity import DefaultAzureCredential, InteractiveBrowserCredential
```

## တစ်ခုခုမှာ ပိတ်မိနေပါသလား?

ဒီ setup ကို run လုပ်ရာမှာ ပြဿနာတစ်ခုခုရှိပါက <a href="https://discord.gg/kzRShWzttr" target="_blank">Azure AI Community Discord</a> ကို join လုပ်ပါ သို့မဟုတ် <a href="https://github.com/microsoft/ai-agents-for-beginners/issues?WT.mc_id=academic-105485-koreyst" target="_blank">issue တစ်ခုဖန်တီးပါ</a>။

## နောက်သင်ခန်းစာ

အခု သင့်မှာ ဒီသင်တန်းရဲ့ ကုဒ်တွေကို run လုပ်ဖို့ ပြင်ဆင်ပြီးပါပြီ။ AI Agents ရဲ့ ကမ္ဘာကို ပိုမိုလေ့လာဖို့ သင့်ကိုယ်ပိုင် အချိန်ယူပြီး သင်ယူပါ။

[AI Agents နဲ့ Agent Use Cases မိတ်ဆက်](../01-intro-to-ai-agents/README.md)

---

**အကြောင်းကြားချက်**:  
ဤစာရွက်စာတမ်းကို AI ဘာသာပြန်ဝန်ဆောင်မှု [Co-op Translator](https://github.com/Azure/co-op-translator) ကို အသုံးပြု၍ ဘာသာပြန်ထားပါသည်။ ကျွန်ုပ်တို့သည် တိကျမှန်ကန်မှုအတွက် ကြိုးစားနေသော်လည်း၊ အလိုအလျောက် ဘာသာပြန်ခြင်းတွင် အမှားများ သို့မဟုတ် မမှန်ကန်မှုများ ပါဝင်နိုင်သည်ကို သတိပြုပါ။ မူရင်းဘာသာစကားဖြင့် ရေးသားထားသော စာရွက်စာတမ်းကို အာဏာတရားရှိသော ရင်းမြစ်အဖြစ် သတ်မှတ်သင့်ပါသည်။ အရေးကြီးသော အချက်အလက်များအတွက် လူက ဘာသာပြန်ခြင်းကို အကြံပြုပါသည်။ ဤဘာသာပြန်ကို အသုံးပြုခြင်းမှ ဖြစ်ပေါ်လာသော အလွဲအလွတ်များ သို့မဟုတ် အနားယူမှားမှုများအတွက် ကျွန်ုပ်တို့သည် တာဝန်မယူပါ။