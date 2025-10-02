<!--
CO_OP_TRANSLATOR_METADATA:
{
  "original_hash": "9b03446058b4eed46928ae5e46325ea0",
  "translation_date": "2025-10-02T19:15:47+00:00",
  "source_file": "00-course-setup/README.md",
  "language_code": "hk"
}
-->
# 課程設置

## 簡介

本課程將介紹如何運行課程中的代碼示例。

## 加入其他學員並獲得幫助

在克隆您的倉庫之前，請加入 [AI Agents For Beginners Discord 頻道](https://aka.ms/ai-agents/discord)，以獲得設置幫助、課程相關問題的解答，或與其他學員交流。

## 克隆或分叉此倉庫

首先，請克隆或分叉 GitHub 倉庫。這將創建您自己的課程材料版本，方便您運行、測試和調整代碼！

您可以點擊以下鏈接來 <a href="https://github.com/microsoft/ai-agents-for-beginners/fork" target="_blank">分叉倉庫</a>。

現在，您應該擁有課程的分叉版本，鏈接如下：

![分叉倉庫](../../../translated_images/forked-repo.33f27ca1901baa6a5e13ec3eb1f0ddd3a44d936d91cc8cfb19bfdb9688bd2c3d.hk.png)

## 運行代碼

本課程提供了一系列 Jupyter Notebook，讓您能夠親身體驗構建 AI Agents 的過程。

代碼示例使用以下選項：

**需要 GitHub 帳戶 - 免費**：

1) Semantic Kernel Agent Framework + GitHub Models Marketplace，標記為 (semantic-kernel.ipynb)
2) AutoGen Framework + GitHub Models Marketplace，標記為 (autogen.ipynb)

**需要 Azure 訂閱**：
3) Azure AI Foundry + Azure AI Agent Service，標記為 (azureaiagent.ipynb)

我們鼓勵您嘗試所有三種類型的示例，以了解哪一種最適合您。

無論您選擇哪個選項，都將決定您需要遵循以下的設置步驟：

## 要求

- Python 3.12+
  - **注意**：如果您尚未安裝 Python 3.12，請確保安裝它。然後使用 python3.12 創建虛擬環境，以確保從 requirements.txt 文件中安裝正確的版本。
  
    >示例

    創建 Python 虛擬環境目錄：

    ``` bash
    python3 -m venv venv
    ```

    然後激活虛擬環境：

    macOS 和 Linux

    ```bash
    source venv/bin/activate
    ```
  
    Windows

    ```bash
    venv\Scripts\activate
    ```

- GitHub 帳戶 - 用於訪問 GitHub Models Marketplace
- Azure 訂閱 - 用於訪問 Azure AI Foundry
- Azure AI Foundry 帳戶 - 用於訪問 Azure AI Agent Service

我們在倉庫的根目錄中包含了一個 `requirements.txt` 文件，其中列出了運行代碼示例所需的所有 Python 包。

您可以在終端中運行以下命令來安裝它們：

```bash
pip install -r requirements.txt
```
我們建議創建一個 Python 虛擬環境，以避免任何衝突和問題。

## 設置 VSCode
確保您在 VSCode 中使用正確版本的 Python。

![image](https://github.com/user-attachments/assets/a85e776c-2edb-4331-ae5b-6bfdfb98ee0e)

## 使用 GitHub Models 的示例設置 

### 步驟 1：獲取您的 GitHub 個人訪問令牌 (PAT)

本課程利用 GitHub Models Marketplace，提供免費訪問大型語言模型 (LLMs)，您將使用它們來構建 AI Agents。

要使用 GitHub Models，您需要創建 [GitHub 個人訪問令牌](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/managing-your-personal-access-tokens)。

您可以通過訪問 GitHub 帳戶中的 <a href="https://github.com/settings/personal-access-tokens" target="_blank">個人訪問令牌設置</a> 來完成此操作。

請遵循 [最小權限原則](https://docs.github.com/en/get-started/learning-to-code/storing-your-secrets-safely) 創建令牌。這意味著您應僅授予令牌運行本課程代碼示例所需的權限。

1. 在屏幕左側選擇 `Fine-grained tokens` 選項，進入 **Developer settings**。
   ![](../../../translated_images/profile_developer_settings.410a859fe749c755c859d414294c5908e307222b2c61819c3203bbeed4470e25.hk.png)

    然後選擇 `Generate new token`。

    ![生成令牌](../../../translated_images/fga_new_token.1c1a234afe202ab37483944a291ee80c1868e1e78082fd6bd4180fea5d5a15b4.hk.png)

2. 為您的令牌輸入一個描述性名稱，反映其用途，方便日後識別。

    🔐 令牌有效期建議

    建議有效期：30 天  
    為了更安全，您可以選擇更短的期限，例如 7 天 🛡️  
    這是一個很好的方式來設置個人目標，並在學習動力高漲時完成課程 🚀。

    ![令牌名稱和到期日期](../../../translated_images/token-name-expiry-date.a095fb0de63868640a4c82d6b1bbc92b482930a663917a5983a3c7cd1ef86b77.hk.png)

3. 將令牌的範圍限制為此倉庫的分叉版本。

    ![限制範圍到分叉倉庫](../../../translated_images/token_repository_limit.924ade5e11d9d8bb6cd21293987e4579dea860e2ba66d607fb46e49524d53644.hk.png)

4. 限制令牌的權限：在 **Permissions** 下，點擊 **Account** 標籤，然後點擊 "+ Add permissions" 按鈕。下拉菜單會出現，請搜索 **Models** 並勾選它。
    ![添加 Models 權限](../../../translated_images/add_models_permissions.c0c44ed8b40fc143dc87792da9097d715b7de938354e8f771d65416ecc7816b8.hk.png)

5. 在生成令牌之前，驗證所需的權限。 ![驗證權限](../../../translated_images/verify_permissions.06bd9e43987a8b219f171bbcf519e45ababae35b844f5e9757e10afcb619b936.hk.png)

6. 在生成令牌之前，確保您準備好將令牌存儲在安全的地方，例如密碼管理器保險庫，因為生成後將無法再次查看。 ![安全存儲令牌](../../../translated_images/store_token_securely.08ee2274c6ad6caf3482f1cd1bad7ca3fdca1ce737bc485bfa6499c84297c789.hk.png)

複製您剛剛創建的新令牌。接下來，您需要將其添加到課程中包含的 `.env` 文件中。

### 步驟 2：創建您的 `.env` 文件

要創建 `.env` 文件，請在終端中運行以下命令：

```bash
cp .env.example .env
```

這將複製示例文件並在您的目錄中創建 `.env` 文件，您需要在其中填寫環境變量的值。

複製您的令牌，然後使用您喜愛的文本編輯器打開 `.env` 文件，將令牌粘貼到 `GITHUB_TOKEN` 字段中。
![GitHub Token 字段](../../../translated_images/github_token_field.20491ed3224b5f4ab24d10ced7a68c4aba2948fe8999cfc8675edaa16f5e5681.hk.png)

現在，您應該能夠運行本課程的代碼示例。

## 使用 Azure AI Foundry 和 Azure AI Agent Service 的示例設置

### 步驟 1：獲取您的 Azure 項目端點

按照此處的步驟創建 Azure AI Foundry 中的 hub 和項目：[Hub 資源概述](https://learn.microsoft.com/en-us/azure/ai-foundry/concepts/ai-resources)

創建項目後，您需要獲取項目的連接字符串。

您可以在 Azure AI Foundry 入口網站的項目 **概述** 頁面找到它。

![項目連接字符串](../../../translated_images/project-endpoint.8cf04c9975bbfbf18f6447a599550edb052e52264fb7124d04a12e6175e330a5.hk.png)

### 步驟 2：創建您的 `.env` 文件

要創建 `.env` 文件，請在終端中運行以下命令：

```bash
cp .env.example .env
```

這將複製示例文件並在您的目錄中創建 `.env` 文件，您需要在其中填寫環境變量的值。

複製您的令牌，然後使用您喜愛的文本編輯器打開 `.env` 文件，將令牌粘貼到 `PROJECT_ENDPOINT` 字段中。

### 步驟 3：登錄 Azure

作為安全最佳實踐，我們將使用 [無密鑰身份驗證](https://learn.microsoft.com/azure/developer/ai/keyless-connections?tabs=csharp%2Cazure-cli?WT.mc_id=academic-105485-koreyst) 通過 Microsoft Entra ID 驗證到 Azure OpenAI。

接下來，打開終端並運行 `az login --use-device-code` 登錄到您的 Azure 帳戶。

登錄後，在終端中選擇您的訂閱。

## 額外的環境變量 - Azure Search 和 Azure OpenAI 

在 Agentic RAG 課程 - 第 5 課中，有一些示例使用了 Azure Search 和 Azure OpenAI。

如果您希望運行這些示例，您需要在 `.env` 文件中添加以下環境變量：

### 概述頁面（項目）

- `AZURE_SUBSCRIPTION_ID` - 在項目 **概述** 頁面的 **項目詳情** 中查看。

- `AZURE_AI_PROJECT_NAME` - 在項目 **概述** 頁面的頂部查看。

- `AZURE_OPENAI_SERVICE` - 在 **概述** 頁面的 **包含的功能** 標籤中找到 **Azure OpenAI Service**。

### 管理中心

- `AZURE_OPENAI_RESOURCE_GROUP` - 在 **管理中心** 的 **概述** 頁面的 **項目屬性** 中查看。

- `GLOBAL_LLM_SERVICE` - 在 **連接的資源** 下找到 **Azure AI Services** 連接名稱。如果未列出，請在 **Azure 入口網站** 中查看您的資源組下的 AI Services 資源名稱。

### 模型 + 端點頁面

- `AZURE_OPENAI_EMBEDDING_DEPLOYMENT_NAME` - 選擇您的嵌入模型（例如 `text-embedding-ada-002`），並記下模型詳情中的 **部署名稱**。

- `AZURE_OPENAI_CHAT_DEPLOYMENT_NAME` - 選擇您的聊天模型（例如 `gpt-4o-mini`），並記下模型詳情中的 **部署名稱**。

### Azure 入口網站

- `AZURE_OPENAI_ENDPOINT` - 查找 **Azure AI Services**，點擊它，然後進入 **資源管理**，選擇 **密鑰和端點**，向下滾動到 "Azure OpenAI 端點"，複製標記為 "Language APIs" 的端點。

- `AZURE_OPENAI_API_KEY` - 在同一屏幕中，複製密鑰 1 或密鑰 2。

- `AZURE_SEARCH_SERVICE_ENDPOINT` - 找到您的 **Azure AI Search** 資源，點擊它，查看 **概述**。

- `AZURE_SEARCH_API_KEY` - 然後進入 **設置**，選擇 **密鑰**，複製主要或次要管理密鑰。

### 外部網頁

- `AZURE_OPENAI_API_VERSION` - 訪問 [API 版本生命周期](https://learn.microsoft.com/en-us/azure/ai-services/openai/api-version-deprecation#latest-ga-api-release) 頁面，查看 **最新 GA API 發布**。

### 設置無密鑰身份驗證

為避免硬編碼憑據，我們將使用 Azure OpenAI 的無密鑰連接。為此，我們將導入 `DefaultAzureCredential`，稍後調用 `DefaultAzureCredential` 函數以獲取憑據。

```python
from azure.identity import DefaultAzureCredential, InteractiveBrowserCredential
```

## 遇到問題？

如果您在設置過程中遇到任何問題，請加入我們的 <a href="https://discord.gg/kzRShWzttr" target="_blank">Azure AI 社區 Discord</a> 或 <a href="https://github.com/microsoft/ai-agents-for-beginners/issues?WT.mc_id=academic-105485-koreyst" target="_blank">創建問題</a>。

## 下一課程

您現在已準備好運行本課程的代碼。祝您在 AI Agents 的世界中學習愉快！

[AI Agents 簡介及應用案例](../01-intro-to-ai-agents/README.md)

---

**免責聲明**：  
本文件已使用人工智能翻譯服務 [Co-op Translator](https://github.com/Azure/co-op-translator) 進行翻譯。儘管我們致力於提供準確的翻譯，請注意自動翻譯可能包含錯誤或不準確之處。原始文件的母語版本應被視為權威來源。對於重要信息，建議使用專業人工翻譯。我們對因使用此翻譯而引起的任何誤解或錯誤解釋概不負責。