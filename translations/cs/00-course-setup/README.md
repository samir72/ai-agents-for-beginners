<!--
CO_OP_TRANSLATOR_METADATA:
{
  "original_hash": "9b03446058b4eed46928ae5e46325ea0",
  "translation_date": "2025-10-02T19:20:48+00:00",
  "source_file": "00-course-setup/README.md",
  "language_code": "cs"
}
-->
# Nastavení kurzu

## Úvod

Tato lekce se zaměřuje na spuštění ukázkového kódu z tohoto kurzu.

## Připojte se k ostatním studentům a získejte pomoc

Než začnete klonovat svůj repozitář, připojte se na [Discord kanál AI Agents For Beginners](https://aka.ms/ai-agents/discord), kde můžete získat pomoc s nastavením, odpovědi na otázky ohledně kurzu nebo se spojit s ostatními studenty.

## Klonování nebo forkování tohoto repozitáře

Začněte klonováním nebo forkováním GitHub repozitáře. Tím si vytvoříte vlastní verzi materiálů kurzu, abyste mohli spouštět, testovat a upravovat kód!

To můžete udělat kliknutím na odkaz <a href="https://github.com/microsoft/ai-agents-for-beginners/fork" target="_blank">fork repozitáře</a>.

Nyní byste měli mít vlastní forkovanou verzi tohoto kurzu na následujícím odkazu:

![Forkovaný repozitář](../../../translated_images/forked-repo.33f27ca1901baa6a5e13ec3eb1f0ddd3a44d936d91cc8cfb19bfdb9688bd2c3d.cs.png)

## Spouštění kódu

Tento kurz nabízí sérii Jupyter Notebooků, které můžete spouštět, abyste získali praktické zkušenosti s tvorbou AI agentů.

Ukázky kódu využívají:

**Vyžaduje GitHub účet - zdarma**:

1) Semantic Kernel Agent Framework + GitHub Models Marketplace. Označeno jako (semantic-kernel.ipynb)
2) AutoGen Framework + GitHub Models Marketplace. Označeno jako (autogen.ipynb)

**Vyžaduje Azure předplatné**:
3) Azure AI Foundry + Azure AI Agent Service. Označeno jako (azureaiagent.ipynb)

Doporučujeme vyzkoušet všechny tři typy příkladů, abyste zjistili, který vám nejlépe vyhovuje.

Podle toho, kterou možnost si vyberete, budete muset postupovat podle příslušných kroků nastavení níže:

## Požadavky

- Python 3.12+
  - **POZNÁMKA**: Pokud nemáte nainstalovaný Python 3.12, ujistěte se, že jej nainstalujete. Poté vytvořte svůj venv pomocí python3.12, abyste zajistili instalaci správných verzí z requirements.txt souboru.
  
    >Příklad

    Vytvořte adresář Python venv:

    ``` bash
    python3 -m venv venv
    ```

    Poté aktivujte venv prostředí pro:

    macOS a Linux

    ```bash
    source venv/bin/activate
    ```
  
    Windows

    ```bash
    venv\Scripts\activate
    ```

- GitHub účet - pro přístup k GitHub Models Marketplace
- Azure předplatné - pro přístup k Azure AI Foundry
- Azure AI Foundry účet - pro přístup k Azure AI Agent Service

V kořenovém adresáři tohoto repozitáře jsme zahrnuli soubor `requirements.txt`, který obsahuje všechny požadované Python balíčky pro spuštění ukázek kódu.

Můžete je nainstalovat spuštěním následujícího příkazu v terminálu v kořenovém adresáři repozitáře:

```bash
pip install -r requirements.txt
```
Doporučujeme vytvořit Python virtuální prostředí, abyste předešli konfliktům a problémům.

## Nastavení VSCode
Ujistěte se, že používáte správnou verzi Pythonu ve VSCode.

![image](https://github.com/user-attachments/assets/a85e776c-2edb-4331-ae5b-6bfdfb98ee0e)

## Nastavení pro ukázky využívající GitHub Models 

### Krok 1: Získání GitHub Personal Access Token (PAT)

Tento kurz využívá GitHub Models Marketplace, který poskytuje bezplatný přístup k modelům velkých jazykových modelů (LLMs), které budete používat k tvorbě AI agentů.

Pro použití GitHub Models budete muset vytvořit [GitHub Personal Access Token](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/managing-your-personal-access-tokens).

To můžete udělat přechodem na <a href="https://github.com/settings/personal-access-tokens" target="_blank">nastavení Personal Access Tokens</a> ve vašem GitHub účtu.

Postupujte podle [Principu minimálních oprávnění](https://docs.github.com/en/get-started/learning-to-code/storing-your-secrets-safely) při vytváření tokenu. To znamená, že byste měli tokenu přidělit pouze oprávnění, která jsou nezbytná pro spuštění ukázek kódu v tomto kurzu.

1. Na levé straně obrazovky vyberte možnost `Fine-grained tokens` v sekci **Developer settings**.
   ![](../../../translated_images/profile_developer_settings.410a859fe749c755c859d414294c5908e307222b2c61819c3203bbeed4470e25.cs.png)

    Poté vyberte `Generate new token`.

    ![Vytvořit token](../../../translated_images/fga_new_token.1c1a234afe202ab37483944a291ee80c1868e1e78082fd6bd4180fea5d5a15b4.cs.png)

2. Zadejte popisný název pro váš token, který odráží jeho účel, aby bylo snadné jej později identifikovat.


    🔐 Doporučení pro dobu platnosti tokenu

    Doporučená doba platnosti: 30 dní  
    Pro větší bezpečnost můžete zvolit kratší dobu, například 7 dní 🛡️  
    Je to skvělý způsob, jak si stanovit osobní cíl a dokončit kurz, zatímco vaše učební motivace je vysoká 🚀.

    ![Název tokenu a datum vypršení platnosti](../../../translated_images/token-name-expiry-date.a095fb0de63868640a4c82d6b1bbc92b482930a663917a5983a3c7cd1ef86b77.cs.png)

3. Omezte rozsah tokenu na váš fork tohoto repozitáře.

    ![Omezit rozsah na fork repozitáře](../../../translated_images/token_repository_limit.924ade5e11d9d8bb6cd21293987e4579dea860e2ba66d607fb46e49524d53644.cs.png)

4. Omezte oprávnění tokenu: V sekci **Permissions** klikněte na záložku **Account** a poté na tlačítko "+ Add permissions". Zobrazí se rozbalovací nabídka. Vyhledejte **Models** a zaškrtněte políčko.
    ![Přidat oprávnění Models](../../../translated_images/add_models_permissions.c0c44ed8b40fc143dc87792da9097d715b7de938354e8f771d65416ecc7816b8.cs.png)

5. Ověřte požadovaná oprávnění před vytvořením tokenu. ![Ověřit oprávnění](../../../translated_images/verify_permissions.06bd9e43987a8b219f171bbcf519e45ababae35b844f5e9757e10afcb619b936.cs.png)

6. Před vytvořením tokenu se ujistěte, že jste připraveni token uložit na bezpečné místo, například do trezoru správce hesel, protože po jeho vytvoření již nebude zobrazen. ![Bezpečně uložit token](../../../translated_images/store_token_securely.08ee2274c6ad6caf3482f1cd1bad7ca3fdca1ce737bc485bfa6499c84297c789.cs.png)

Zkopírujte svůj nový token, který jste právě vytvořili. Nyní jej přidáte do souboru `.env` zahrnutého v tomto kurzu.


### Krok 2: Vytvoření souboru `.env`

Pro vytvoření souboru `.env` spusťte následující příkaz ve svém terminálu.

```bash
cp .env.example .env
```

Tím se zkopíruje příkladový soubor a vytvoří `.env` ve vašem adresáři, kde vyplníte hodnoty pro proměnné prostředí.

S tokenem zkopírovaným, otevřete soubor `.env` ve svém oblíbeném textovém editoru a vložte token do pole `GITHUB_TOKEN`.
![Pole GitHub Token](../../../translated_images/github_token_field.20491ed3224b5f4ab24d10ced7a68c4aba2948fe8999cfc8675edaa16f5e5681.cs.png)


Nyní byste měli být schopni spustit ukázky kódu z tohoto kurzu.

## Nastavení pro ukázky využívající Azure AI Foundry a Azure AI Agent Service

### Krok 1: Získání Azure Project Endpoint


Postupujte podle kroků pro vytvoření hubu a projektu v Azure AI Foundry zde: [Přehled zdrojů hubu](https://learn.microsoft.com/en-us/azure/ai-foundry/concepts/ai-resources)


Jakmile vytvoříte svůj projekt, budete muset získat připojovací řetězec pro váš projekt.

To lze provést přechodem na stránku **Overview** vašeho projektu v portálu Azure AI Foundry.

![Připojovací řetězec projektu](../../../translated_images/project-endpoint.8cf04c9975bbfbf18f6447a599550edb052e52264fb7124d04a12e6175e330a5.cs.png)

### Krok 2: Vytvoření souboru `.env`

Pro vytvoření souboru `.env` spusťte následující příkaz ve svém terminálu.

```bash
cp .env.example .env
```

Tím se zkopíruje příkladový soubor a vytvoří `.env` ve vašem adresáři, kde vyplníte hodnoty pro proměnné prostředí.

S tokenem zkopírovaným, otevřete soubor `.env` ve svém oblíbeném textovém editoru a vložte token do pole `PROJECT_ENDPOINT`.

### Krok 3: Přihlášení do Azure

Jako bezpečnostní nejlepší praxi použijeme [autentizaci bez klíče](https://learn.microsoft.com/azure/developer/ai/keyless-connections?tabs=csharp%2Cazure-cli?WT.mc_id=academic-105485-koreyst) pro autentizaci do Azure OpenAI pomocí Microsoft Entra ID. 

Otevřete terminál a spusťte `az login --use-device-code` pro přihlášení do svého Azure účtu.

Jakmile se přihlásíte, vyberte své předplatné v terminálu.


## Další proměnné prostředí - Azure Search a Azure OpenAI 

Pro lekci Agentic RAG - Lekce 5 - jsou zde ukázky, které využívají Azure Search a Azure OpenAI.

Pokud chcete tyto ukázky spustit, budete muset přidat následující proměnné prostředí do svého souboru `.env`:

### Stránka přehledu (Projekt)

- `AZURE_SUBSCRIPTION_ID` - Zkontrolujte **Project details** na stránce **Overview** vašeho projektu.

- `AZURE_AI_PROJECT_NAME` - Podívejte se na horní část stránky **Overview** vašeho projektu.

- `AZURE_OPENAI_SERVICE` - Najděte to na záložce **Included capabilities** pro **Azure OpenAI Service** na stránce **Overview**.

### Centrum správy

- `AZURE_OPENAI_RESOURCE_GROUP` - Přejděte na **Project properties** na stránce **Overview** v **Management Center**.

- `GLOBAL_LLM_SERVICE` - Pod **Connected resources** najděte název připojení **Azure AI Services**. Pokud není uveden, zkontrolujte **Azure portal** pod vaší skupinou zdrojů pro název zdroje AI Services.

### Stránka Models + Endpoints

- `AZURE_OPENAI_EMBEDDING_DEPLOYMENT_NAME` - Vyberte svůj embedding model (např. `text-embedding-ada-002`) a poznamenejte si **Deployment name** z detailů modelu.

- `AZURE_OPENAI_CHAT_DEPLOYMENT_NAME` - Vyberte svůj chat model (např. `gpt-4o-mini`) a poznamenejte si **Deployment name** z detailů modelu.

### Azure Portal

- `AZURE_OPENAI_ENDPOINT` - Najděte **Azure AI services**, klikněte na něj, poté přejděte na **Resource Management**, **Keys and Endpoint**, sjeďte dolů na "Azure OpenAI endpoints" a zkopírujte ten, který říká "Language APIs".

- `AZURE_OPENAI_API_KEY` - Na stejné obrazovce zkopírujte KEY 1 nebo KEY 2.

- `AZURE_SEARCH_SERVICE_ENDPOINT` - Najděte svůj **Azure AI Search** zdroj, klikněte na něj a podívejte se na **Overview**.

- `AZURE_SEARCH_API_KEY` - Poté přejděte na **Settings** a poté **Keys**, abyste zkopírovali primární nebo sekundární administrátorský klíč.

### Externí webová stránka

- `AZURE_OPENAI_API_VERSION` - Navštivte stránku [API version lifecycle](https://learn.microsoft.com/en-us/azure/ai-services/openai/api-version-deprecation#latest-ga-api-release) pod **Latest GA API release**.

### Nastavení autentizace bez klíče

Namísto pevného kódování vašich přihlašovacích údajů použijeme připojení bez klíče s Azure OpenAI. K tomu importujeme `DefaultAzureCredential` a později zavoláme funkci `DefaultAzureCredential`, abychom získali přihlašovací údaje.

```python
from azure.identity import DefaultAzureCredential, InteractiveBrowserCredential
```

## Máte problém?

Pokud máte jakékoli problémy s tímto nastavením, připojte se na náš <a href="https://discord.gg/kzRShWzttr" target="_blank">Discord Azure AI Community</a> nebo <a href="https://github.com/microsoft/ai-agents-for-beginners/issues?WT.mc_id=academic-105485-koreyst" target="_blank">vytvořte issue</a>.

## Další lekce

Nyní jste připraveni spustit kód tohoto kurzu. Přejeme vám příjemné učení o světě AI agentů! 

[Úvod do AI agentů a jejich využití](../01-intro-to-ai-agents/README.md)

---

**Prohlášení**:  
Tento dokument byl přeložen pomocí služby AI pro překlady [Co-op Translator](https://github.com/Azure/co-op-translator). I když se snažíme o přesnost, mějte prosím na paměti, že automatizované překlady mohou obsahovat chyby nebo nepřesnosti. Původní dokument v jeho původním jazyce by měl být považován za autoritativní zdroj. Pro důležité informace se doporučuje profesionální lidský překlad. Neodpovídáme za žádná nedorozumění nebo nesprávné interpretace vyplývající z použití tohoto překladu.