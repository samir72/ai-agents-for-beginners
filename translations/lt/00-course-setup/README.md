<!--
CO_OP_TRANSLATOR_METADATA:
{
  "original_hash": "9b03446058b4eed46928ae5e46325ea0",
  "translation_date": "2025-10-02T19:26:08+00:00",
  "source_file": "00-course-setup/README.md",
  "language_code": "lt"
}
-->
# Kursų nustatymas

## Įvadas

Šioje pamokoje aptarsime, kaip paleisti šio kurso kodo pavyzdžius.

## Prisijunkite prie kitų mokinių ir gaukite pagalbos

Prieš pradėdami klonuoti savo saugyklą, prisijunkite prie [AI Agents For Beginners Discord kanalo](https://aka.ms/ai-agents/discord), kad gautumėte pagalbos dėl nustatymo, užduotumėte klausimus apie kursą ar susisiektumėte su kitais mokiniais.

## Klonuokite arba „forkinkite“ šią saugyklą

Norėdami pradėti, prašome klonuoti arba „forkinti“ GitHub saugyklą. Tai sukurs jūsų asmeninę kurso medžiagos versiją, kad galėtumėte paleisti, testuoti ir koreguoti kodą!

Tai galite padaryti paspaudę nuorodą <a href="https://github.com/microsoft/ai-agents-for-beginners/fork" target="_blank">forkinti saugyklą</a>.

Dabar turėtumėte turėti savo „forkintą“ šio kurso versiją šioje nuorodoje:

![Forkinta saugykla](../../../translated_images/forked-repo.33f27ca1901baa6a5e13ec3eb1f0ddd3a44d936d91cc8cfb19bfdb9688bd2c3d.lt.png)

## Kodo paleidimas

Šis kursas siūlo seriją Jupyter Notebook failų, kuriuos galite paleisti, kad praktiškai išbandytumėte AI agentų kūrimą.

Kodo pavyzdžiai naudoja:

**Reikalinga GitHub paskyra - nemokama**:

1) Semantic Kernel Agent Framework + GitHub Models Marketplace. Pažymėta kaip (semantic-kernel.ipynb)
2) AutoGen Framework + GitHub Models Marketplace. Pažymėta kaip (autogen.ipynb)

**Reikalinga Azure prenumerata**:
3) Azure AI Foundry + Azure AI Agent Service. Pažymėta kaip (azureaiagent.ipynb)

Rekomenduojame išbandyti visus tris pavyzdžių tipus, kad pamatytumėte, kuris jums geriausiai tinka.

Pasirinktas variantas nulems, kokius nustatymo veiksmus turėsite atlikti toliau:

## Reikalavimai

- Python 3.12+
  - **PASTABA**: Jei neturite įdiegto Python 3.12, įsitikinkite, kad jį įdiegėte. Tada sukurkite savo venv naudodami python3.12, kad užtikrintumėte, jog iš `requirements.txt` failo bus įdiegtos tinkamos versijos.
  
    >Pavyzdys

    Sukurkite Python venv katalogą:

    ``` bash
    python3 -m venv venv
    ```

    Tada aktyvuokite venv aplinką:

    macOS ir Linux

    ```bash
    source venv/bin/activate
    ```
  
    Windows

    ```bash
    venv\Scripts\activate
    ```

- GitHub paskyra - prieiga prie GitHub Models Marketplace
- Azure prenumerata - prieiga prie Azure AI Foundry
- Azure AI Foundry paskyra - prieiga prie Azure AI Agent Service

Šios saugyklos šakniniame kataloge įtraukėme `requirements.txt` failą, kuriame yra visi reikalingi Python paketai, kad galėtumėte paleisti kodo pavyzdžius.

Juos galite įdiegti paleisdami šią komandą terminale saugyklos šakniniame kataloge:

```bash
pip install -r requirements.txt
```
Rekomenduojame sukurti Python virtualią aplinką, kad išvengtumėte konfliktų ir problemų.

## VSCode nustatymas
Įsitikinkite, kad naudojate tinkamą Python versiją VSCode.

![image](https://github.com/user-attachments/assets/a85e776c-2edb-4331-ae5b-6bfdfb98ee0e)

## Nustatymas pavyzdžiams naudojant GitHub modelius 

### 1 žingsnis: Gaukite savo GitHub asmeninį prieigos raktą (PAT)

Šis kursas naudoja GitHub Models Marketplace, kuris suteikia nemokamą prieigą prie didelių kalbos modelių (LLMs), kuriuos naudosite AI agentų kūrimui.

Norėdami naudoti GitHub modelius, turėsite sukurti [GitHub asmeninį prieigos raktą](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/managing-your-personal-access-tokens).

Tai galite padaryti savo GitHub paskyroje, eidami į <a href="https://github.com/settings/personal-access-tokens" target="_blank">Asmeninių prieigos raktų nustatymus</a>.

Prašome laikytis [mažiausios privilegijos principo](https://docs.github.com/en/get-started/learning-to-code/storing-your-secrets-safely) kuriant savo raktą. Tai reiškia, kad turėtumėte suteikti raktui tik tas teises, kurios būtinos šio kurso kodo pavyzdžiams paleisti.

1. Kairėje ekrano pusėje pasirinkite `Fine-grained tokens` parinktį, eidami į **Developer settings**.
   ![](../../../translated_images/profile_developer_settings.410a859fe749c755c859d414294c5908e307222b2c61819c3203bbeed4470e25.lt.png)

    Tada pasirinkite `Generate new token`.

    ![Sukurti raktą](../../../translated_images/fga_new_token.1c1a234afe202ab37483944a291ee80c1868e1e78082fd6bd4180fea5d5a15b4.lt.png)

2. Įveskite aprašomąjį pavadinimą savo raktui, kuris atspindi jo paskirtį, kad vėliau būtų lengva jį identifikuoti.


    🔐 Rekomendacija dėl rakto galiojimo trukmės

    Rekomenduojama trukmė: 30 dienų  
    Dėl saugumo galite pasirinkti trumpesnį laikotarpį, pvz., 7 dienas 🛡️  
    Tai puikus būdas nustatyti asmeninį tikslą ir baigti kursą, kol jūsų mokymosi tempas yra aukštas 🚀.

    ![Rakto pavadinimas ir galiojimo data](../../../translated_images/token-name-expiry-date.a095fb0de63868640a4c82d6b1bbc92b482930a663917a5983a3c7cd1ef86b77.lt.png)

3. Apribokite rakto taikymo sritį savo „forkintai“ šios saugyklos versijai.

    ![Apriboti taikymo sritį „forkintai“ saugyklai](../../../translated_images/token_repository_limit.924ade5e11d9d8bb6cd21293987e4579dea860e2ba66d607fb46e49524d53644.lt.png)

4. Apribokite rakto teises: Skiltyje **Permissions** spustelėkite **Account** skirtuką ir paspauskite "+ Add permissions" mygtuką. Atsiras išskleidžiamasis meniu. Prašome ieškoti **Models** ir pažymėti langelį.

    ![Pridėti modelių teises](../../../translated_images/add_models_permissions.c0c44ed8b40fc143dc87792da9097d715b7de938354e8f771d65416ecc7816b8.lt.png)

5. Patikrinkite reikalingas teises prieš generuodami raktą. ![Patikrinti teises](../../../translated_images/verify_permissions.06bd9e43987a8b219f171bbcf519e45ababae35b844f5e9757e10afcb619b936.lt.png)

6. Prieš generuodami raktą, įsitikinkite, kad esate pasiruošę saugiai jį laikyti, pvz., slaptažodžių tvarkyklės saugykloje, nes jis nebus rodomas dar kartą po sukūrimo. ![Saugiai laikyti raktą](../../../translated_images/store_token_securely.08ee2274c6ad6caf3482f1cd1bad7ca3fdca1ce737bc485bfa6499c84297c789.lt.png)

Nukopijuokite naują raktą, kurį ką tik sukūrėte. Dabar pridėsite jį prie `.env` failo, įtraukto į šį kursą.


### 2 žingsnis: Sukurkite savo `.env` failą

Norėdami sukurti `.env` failą, paleiskite šią komandą terminale.

```bash
cp .env.example .env
```

Tai nukopijuos pavyzdinį failą ir sukurs `.env` jūsų kataloge, kur užpildysite aplinkos kintamųjų reikšmes.

Nukopijavę savo raktą, atidarykite `.env` failą mėgstamame teksto redaktoriuje ir įklijuokite savo raktą į `GITHUB_TOKEN` lauką.
![GitHub rakto laukas](../../../translated_images/github_token_field.20491ed3224b5f4ab24d10ced7a68c4aba2948fe8999cfc8675edaa16f5e5681.lt.png)


Dabar turėtumėte galėti paleisti šio kurso kodo pavyzdžius.

## Nustatymas pavyzdžiams naudojant Azure AI Foundry ir Azure AI Agent Service

### 1 žingsnis: Gaukite savo Azure projekto galutinį tašką

Sekite veiksmus, kaip sukurti centrą ir projektą Azure AI Foundry, pateiktus čia: [Hub resursų apžvalga](https://learn.microsoft.com/en-us/azure/ai-foundry/concepts/ai-resources)

Kai sukursite savo projektą, turėsite gauti projekto prisijungimo eilutę.

Tai galite padaryti eidami į **Overview** puslapį savo projekte Azure AI Foundry portale.

![Projekto prisijungimo eilutė](../../../translated_images/project-endpoint.8cf04c9975bbfbf18f6447a599550edb052e52264fb7124d04a12e6175e330a5.lt.png)

### 2 žingsnis: Sukurkite savo `.env` failą

Norėdami sukurti `.env` failą, paleiskite šią komandą terminale.

```bash
cp .env.example .env
```

Tai nukopijuos pavyzdinį failą ir sukurs `.env` jūsų kataloge, kur užpildysite aplinkos kintamųjų reikšmes.

Nukopijavę savo raktą, atidarykite `.env` failą mėgstamame teksto redaktoriuje ir įklijuokite savo raktą į `PROJECT_ENDPOINT` lauką.

### 3 žingsnis: Prisijunkite prie Azure

Kaip saugumo geriausią praktiką, naudosime [autentifikaciją be rakto](https://learn.microsoft.com/azure/developer/ai/keyless-connections?tabs=csharp%2Cazure-cli?WT.mc_id=academic-105485-koreyst), kad autentifikuotume prie Azure OpenAI su Microsoft Entra ID. 

Tada atidarykite terminalą ir paleiskite `az login --use-device-code`, kad prisijungtumėte prie savo Azure paskyros.

Prisijungę terminale pasirinkite savo prenumeratą.


## Papildomi aplinkos kintamieji - Azure Search ir Azure OpenAI 

Agentic RAG pamokoje - 5 pamokoje - yra pavyzdžių, kurie naudoja Azure Search ir Azure OpenAI.

Jei norite paleisti šiuos pavyzdžius, turėsite pridėti šiuos aplinkos kintamuosius į savo `.env` failą:

### Apžvalgos puslapis (Projektas)

- `AZURE_SUBSCRIPTION_ID` - Patikrinkite **Project details** skiltyje **Overview** puslapyje savo projekte.

- `AZURE_AI_PROJECT_NAME` - Žiūrėkite viršuje **Overview** puslapio savo projekte.

- `AZURE_OPENAI_SERVICE` - Raskite tai **Included capabilities** skirtuke **Azure OpenAI Service** skiltyje **Overview** puslapyje.

### Valdymo centras

- `AZURE_OPENAI_RESOURCE_GROUP` - Eikite į **Project properties** skiltyje **Overview** puslapyje **Management Center**.

- `GLOBAL_LLM_SERVICE` - Skiltyje **Connected resources**, raskite **Azure AI Services** prisijungimo pavadinimą. Jei nerandate, patikrinkite **Azure portalą** savo resursų grupėje dėl AI Services resurso pavadinimo.

### Modeliai + galutiniai taškai puslapis

- `AZURE_OPENAI_EMBEDDING_DEPLOYMENT_NAME` - Pasirinkite savo įterpimo modelį (pvz., `text-embedding-ada-002`) ir užsirašykite **Deployment name** iš modelio detalių.

- `AZURE_OPENAI_CHAT_DEPLOYMENT_NAME` - Pasirinkite savo pokalbių modelį (pvz., `gpt-4o-mini`) ir užsirašykite **Deployment name** iš modelio detalių.

### Azure portalas

- `AZURE_OPENAI_ENDPOINT` - Ieškokite **Azure AI services**, spustelėkite ant jo, tada eikite į **Resource Management**, **Keys and Endpoint**, slinkite žemyn iki "Azure OpenAI endpoints" ir nukopijuokite tą, kuris pažymėtas "Language APIs".

- `AZURE_OPENAI_API_KEY` - Iš to paties ekrano nukopijuokite KEY 1 arba KEY 2.

- `AZURE_SEARCH_SERVICE_ENDPOINT` - Raskite savo **Azure AI Search** resursą, spustelėkite jį ir peržiūrėkite **Overview**.

- `AZURE_SEARCH_API_KEY` - Tada eikite į **Settings** ir tada **Keys**, kad nukopijuotumėte pirminį arba antrinį administratoriaus raktą.

### Išorinė svetainė

- `AZURE_OPENAI_API_VERSION` - Apsilankykite [API versijos gyvavimo ciklo](https://learn.microsoft.com/en-us/azure/ai-services/openai/api-version-deprecation#latest-ga-api-release) puslapyje skiltyje **Latest GA API release**.

### Nustatykite autentifikaciją be rakto

Užuot kodavę savo kredencialus, naudosime autentifikaciją be rakto su Azure OpenAI. Tam importuosime `DefaultAzureCredential` ir vėliau iškviesime `DefaultAzureCredential` funkciją, kad gautume kredencialą.

```python
from azure.identity import DefaultAzureCredential, InteractiveBrowserCredential
```

## Kažkur užstrigote?

Jei turite problemų paleidžiant šį nustatymą, prisijunkite prie mūsų <a href="https://discord.gg/kzRShWzttr" target="_blank">Azure AI bendruomenės Discord</a> arba <a href="https://github.com/microsoft/ai-agents-for-beginners/issues?WT.mc_id=academic-105485-koreyst" target="_blank">sukurkite problemą</a>.

## Kita pamoka

Dabar esate pasiruošę paleisti šio kurso kodą. Smagaus mokymosi apie AI agentų pasaulį! 

[Įvadas į AI agentus ir agentų naudojimo atvejus](../01-intro-to-ai-agents/README.md)

---

**Atsakomybės atsisakymas**:  
Šis dokumentas buvo išverstas naudojant AI vertimo paslaugą [Co-op Translator](https://github.com/Azure/co-op-translator). Nors siekiame tikslumo, prašome atkreipti dėmesį, kad automatiniai vertimai gali turėti klaidų ar netikslumų. Originalus dokumentas jo gimtąja kalba turėtų būti laikomas autoritetingu šaltiniu. Kritinei informacijai rekomenduojama profesionali žmogaus vertimo paslauga. Mes neprisiimame atsakomybės už nesusipratimus ar klaidingus interpretavimus, atsiradusius naudojant šį vertimą.