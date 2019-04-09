---
ms.openlocfilehash: dac06138d5d8dde9fce1ee8a8f0dbfe6bc01d496
ms.sourcegitcommit: e17cc64775307fcf15cef8e0181fdb046ccd227f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/20/2019
ms.locfileid: "58265880"
---
<span data-ttu-id="2a994-101">V Microsoft PowerApps se zdroje dat používají k připojení a ukládání dat.</span><span class="sxs-lookup"><span data-stu-id="2a994-101">In Microsoft PowerApps, you use data sources to connect to and store your data.</span></span>
<span data-ttu-id="2a994-102">Můžete získat přístup k datům v ekosystému Office 365, kam patří Common Data Service (CDS) for Apps, SharePoint, SQL Server a jiné místní zdroje, Azure a jiné cloudové služby, webové rozhraní API nebo kterýkoli z více než 200 integrovaných konektorů.</span><span class="sxs-lookup"><span data-stu-id="2a994-102">You can access data within the Office 365 ecosystem in locations such as Common Data Service (CDS) for Apps, SharePoint, SQL Server, and other on-premises sources; Azure or other cloud services; a web API; or any of more than 200 built-in connectors.</span></span>

<span data-ttu-id="2a994-103">Tento obrázek ukazuje nejběžnější zdroje dat.</span><span class="sxs-lookup"><span data-stu-id="2a994-103">This graphic shows the most common data sources.</span></span>

![Zdroje dat](../media/datasources.png)

<span data-ttu-id="2a994-105">Licence PowerApps Plan 1 a PowerApps Plan 2 poskytují přístup k prémiovým konektorům, mezi které patří:</span><span class="sxs-lookup"><span data-stu-id="2a994-105">The PowerApps Plan 1 and PowerApps Plan 2 licenses provide access to premium connectors, such as these examples:</span></span>

-   <span data-ttu-id="2a994-106">Common Data Service (databáze)</span><span class="sxs-lookup"><span data-stu-id="2a994-106">Common Data Service (database)</span></span>

-   <span data-ttu-id="2a994-107">Salesforce</span><span class="sxs-lookup"><span data-stu-id="2a994-107">Salesforce</span></span>

-   <span data-ttu-id="2a994-108">DocuSign</span><span class="sxs-lookup"><span data-stu-id="2a994-108">DocuSign</span></span>

-   <span data-ttu-id="2a994-109">MailChimp</span><span class="sxs-lookup"><span data-stu-id="2a994-109">MailChimp</span></span>

-   <span data-ttu-id="2a994-110">Oracle</span><span class="sxs-lookup"><span data-stu-id="2a994-110">Oracle</span></span>

-   <span data-ttu-id="2a994-111">ServiceNow</span><span class="sxs-lookup"><span data-stu-id="2a994-111">ServiceNow</span></span>

-   <span data-ttu-id="2a994-112">Workday HCM</span><span class="sxs-lookup"><span data-stu-id="2a994-112">Workday HCM</span></span>

<a name="tabular-or-action-based-data-sources"></a><span data-ttu-id="2a994-113">Zdroje dat založené na tabulkách nebo akcích</span><span class="sxs-lookup"><span data-stu-id="2a994-113">Tabular or action-based data sources</span></span>
------------------------------------

<span data-ttu-id="2a994-114">Zdroje dat poskytují data buď ve formě akcí, nebo jedné či více tabulek.</span><span class="sxs-lookup"><span data-stu-id="2a994-114">Data sources provide data as either actions or one or more tables.</span></span> <span data-ttu-id="2a994-115">Některé zdroje dat, například CDS for Apps, SharePoint a SQL Server, poskytují data ve strukturované tabulce.</span><span class="sxs-lookup"><span data-stu-id="2a994-115">Some data sources, such as CDS for Apps, SharePoint, and SQL Server provide your data in a structured table.</span></span> <span data-ttu-id="2a994-116">U tabulkových zdrojů dat lze data snadno zobrazit v galerii nebo formuláři.</span><span class="sxs-lookup"><span data-stu-id="2a994-116">With table data sources, you can easily display the data in a gallery or a form.</span></span> <span data-ttu-id="2a994-117">V PowerApps můžete pro práci s tabulkami dat používat několik funkcí.</span><span class="sxs-lookup"><span data-stu-id="2a994-117">In PowerApps, you can use multiple functions for working with tables of data.</span></span>

<span data-ttu-id="2a994-118">Jiné zdroje dat, například konektor Uživatelé Office 365 nebo Project Online, jsou založené na akcích.</span><span class="sxs-lookup"><span data-stu-id="2a994-118">Other data sources, such as the Office 365 Users connector or Project Online, are action based.</span></span> <span data-ttu-id="2a994-119">Po připojení k těmto zdrojům dat můžete pomocí různých funkcí spouštět různé akce.</span><span class="sxs-lookup"><span data-stu-id="2a994-119">When you connect to these data sources, you can run different actions by using various functions.</span></span> <span data-ttu-id="2a994-120">Obecně musíte tyto funkce explicitně připojit k ovládacím prvkům, abyste s nimi mohli provádět interakce.</span><span class="sxs-lookup"><span data-stu-id="2a994-120">Generally, you must explicitly connect these functions to controls to interact with them.</span></span> <span data-ttu-id="2a994-121">Nefungují automaticky jako tabulkové zdroje dat.</span><span class="sxs-lookup"><span data-stu-id="2a994-121">They do not work automatically like tabular data sources.</span></span> <span data-ttu-id="2a994-122">Tato funkce se například dotazuje na data.</span><span class="sxs-lookup"><span data-stu-id="2a994-122">For example, this function queries data.</span></span>

```
Office365Users.SearchUser()
```

<span data-ttu-id="2a994-123">Tato funkce naopak aktualizuje data.</span><span class="sxs-lookup"><span data-stu-id="2a994-123">In contrast, this function updates data.</span></span>

```
Office365Users.UpdateMyProfile({aboutMe:"I love PowerApps"})
```

<a name="custom-connectors"></a><span data-ttu-id="2a994-124">Vlastní konektory</span><span class="sxs-lookup"><span data-stu-id="2a994-124">Custom connectors</span></span>
-----------------

<span data-ttu-id="2a994-125">Pokud vaše potřeby nesplňuje žádný integrovaný konektor, můžete si vytvořit vlastní konektor pro dotazování libovolného webového rozhraní API.</span><span class="sxs-lookup"><span data-stu-id="2a994-125">You can create a custom connector to query any web API if no built-in connector suits your needs.</span></span> <span data-ttu-id="2a994-126">K vytvoření vlastního konektoru nemusíte umět psát kód jazyka C\#.</span><span class="sxs-lookup"><span data-stu-id="2a994-126">You don't need to write C\# code to create a custom connector.</span></span> <span data-ttu-id="2a994-127">S využitím prostředí Postman nebo souboru OpenAPI můžete jednoduše vytvořit vlastní konektor.</span><span class="sxs-lookup"><span data-stu-id="2a994-127">You can create your connector with just a few steps by using a Postman or OpenAPI file.</span></span> <span data-ttu-id="2a994-128">Další informace najdete v článku o [vlastních konektorech pro aplikace plátna](https://docs.microsoft.com/powerapps/maker/canvas-apps/register-custom-api).</span><span class="sxs-lookup"><span data-stu-id="2a994-128">For more information, see [Custom connectors for canvas apps](https://docs.microsoft.com/powerapps/maker/canvas-apps/register-custom-api).</span></span>
<span data-ttu-id="2a994-129">Ve zbývající části tohoto studijního programu se probírá, jak přidat zdroj dat, zobrazit data v galerii, sestavit zdroje dat pomocí kolekcí a efektivně pracovat s rozsáhlými datovými sadami pomocí delegování.</span><span class="sxs-lookup"><span data-stu-id="2a994-129">The remainder of this learning path discusses how to add a data source, display data in a gallery, build data sources by using collections, and work with large data sets efficiently by understanding delegation.</span></span> 