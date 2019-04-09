---
ms.openlocfilehash: 2593bbecc1936908d50a58c0bee225cd6765730a
ms.sourcegitcommit: cc419b18821783e2dffd74123baf355c1ef97243
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/14/2019
ms.locfileid: "57806213"
---
<span data-ttu-id="48aee-101">S nainstalovaným Microsoft Power BI Desktopem jste teď připravení se připojit k neustále se zvětšujícímu světu dat.</span><span class="sxs-lookup"><span data-stu-id="48aee-101">Now that Microsoft Power BI Desktop is installed, you're ready to connect to the ever-expanding world of data.</span></span> <span data-ttu-id="48aee-102">Existují *nejrůznější* zdroje dat, které jsou dostupné v okně Microsoft Power Query pro Excel.</span><span class="sxs-lookup"><span data-stu-id="48aee-102">There are *all sorts* of data sources available in the Microsoft Power Query for Excel window.</span></span> <span data-ttu-id="48aee-103">Následující obrázek ukazuje, jak se připojit k datům výběrem karty **Domů** na pásu karet a následně výběrem možností **Získat data \> Více**.</span><span class="sxs-lookup"><span data-stu-id="48aee-103">The following image shows how to connect to data by selecting the **Home** tab on the ribbon and then selecting **Get Data \> More**.</span></span>

![Získání dat](../media/TC-DesktopIntro.gif)

<span data-ttu-id="48aee-105">V této jednotce se připojíme k několika různým **webovým** zdrojům dat.</span><span class="sxs-lookup"><span data-stu-id="48aee-105">In this unit, we'll connect to a couple different **Web** data sources.</span></span>

<span data-ttu-id="48aee-106">Představte si, že odcházíte do důchodu – chcete žít někde, kde je hodně slunce, nízká kriminalita a dobrá zdravotní péče – nebo jste třeba datoví analytici a chcete tyto informace zjistit pro své zákazníky.</span><span class="sxs-lookup"><span data-stu-id="48aee-106">Imagine you’re retiring – you want to live where there’s lots of sunshine, low crime rates, and good health care – or perhaps you’re a data analyst, and you want that information to help your customers.</span></span> <span data-ttu-id="48aee-107">Možná chcete pomoct například vašemu prodejci slunečních brýlí se zacílením prodeje tam, kde nejčastěji svítí slunce.</span><span class="sxs-lookup"><span data-stu-id="48aee-107">For example, maybe you want to help your sunglasses retailer target sales where the sun shines most frequently.</span></span>

<span data-ttu-id="48aee-108">V obou případech obsahuje následující webový prostředek zajímavá data o těchto tématech a mnohem víc:</span><span class="sxs-lookup"><span data-stu-id="48aee-108">Either way, the following web resource has interesting data about those topics, and more:</span></span>

<span data-ttu-id="48aee-109"><a href="https://go.microsoft.com/fwlink/?linkid=2050811" target="_blank">Pořadí států, kde je nejlepší trávit důchod</a></span><span class="sxs-lookup"><span data-stu-id="48aee-109"><a href="https://go.microsoft.com/fwlink/?linkid=2050811" target="_blank">Best places to retire state rank</a></span></span>  


<span data-ttu-id="48aee-110">Vyberte **Načíst data \> Web** a vložte tuto adresu.</span><span class="sxs-lookup"><span data-stu-id="48aee-110">Select **Get Data \> Web**, and paste the address.</span></span>

![Připojení k webovým datům](../media/pbid-getdata_01.jpg)

<span data-ttu-id="48aee-112">Když vyberete **OK**, začne fungovat funkce **dotazu** Power BI Desktopu.</span><span class="sxs-lookup"><span data-stu-id="48aee-112">When you select **OK**, the **Query** functionality of Power BI Desktop goes to work.</span></span> <span data-ttu-id="48aee-113">Dotaz zkontaktuje webový prostředek a okno **Navigátor** zobrazí výsledky nalezené na dané webové stránce.</span><span class="sxs-lookup"><span data-stu-id="48aee-113">Query contacts the web resource, and the **Navigator** window shows what it found on that webpage.</span></span> <span data-ttu-id="48aee-114">V tomto případě našel tabulku (*Table 0*) a celý webový dokument.</span><span class="sxs-lookup"><span data-stu-id="48aee-114">In this case, it finds a table (*Table 0*) and the overall web document.</span></span> <span data-ttu-id="48aee-115">Nás zajímá tabulka, takže ji vyberte v seznamu.</span><span class="sxs-lookup"><span data-stu-id="48aee-115">We're interested in the table, so select it in the list.</span></span> <span data-ttu-id="48aee-116">V okně **Navigátor** se zobrazí náhled.</span><span class="sxs-lookup"><span data-stu-id="48aee-116">The **Navigator** window shows a preview.</span></span>

![Okno Navigátor](../media/pbid-getdata_02.jpg)

<span data-ttu-id="48aee-118">V tomto okamžiku můžete před načtením tabulky dotaz upravit výběrem **Upravit** v dolní části okna.</span><span class="sxs-lookup"><span data-stu-id="48aee-118">At this point, you can edit the query before loading the table, by selecting **Edit** at the bottom of the window.</span></span> <span data-ttu-id="48aee-119">Nebo můžete tabulku rovnou načíst.</span><span class="sxs-lookup"><span data-stu-id="48aee-119">Or, you can just load the table.</span></span>

<span data-ttu-id="48aee-120">Když vyberete **Upravit**, spustí se editor Power Query a zobrazí se reprezentativní zobrazení tabulky.</span><span class="sxs-lookup"><span data-stu-id="48aee-120">When you select **Edit**, Power Query Editor starts, and a representative view of the table is shown.</span></span> <span data-ttu-id="48aee-121">Zobrazí se podokno **Nastavení dotazů** (pokud ne, vyberte na pásu karet kartu **Zobrazení** a pak vyberte **Zobrazit \> Nastavení dotazů**).</span><span class="sxs-lookup"><span data-stu-id="48aee-121">The **Query Settings** pane appears (if it doesn't, select the **View** tab on the ribbon, then select **Show \> Query Settings**).</span></span> <span data-ttu-id="48aee-122">Takhle to vypadá.</span><span class="sxs-lookup"><span data-stu-id="48aee-122">Here's what it looks like.</span></span>

![Okno editoru Power Query](../media/pbid-getdata_03.jpg)

<span data-ttu-id="48aee-124">V Power BI Desktopu se můžete připojit k více zdrojům dat a zkombinovat je, aby bylo možné provádět zajímavé věci.</span><span class="sxs-lookup"><span data-stu-id="48aee-124">In Power BI Desktop, you can connect to multiple data sources and combine them to do interesting things.</span></span> 

<span data-ttu-id="48aee-125">V další jednotce upravíme data přesně podle našich potřeb.</span><span class="sxs-lookup"><span data-stu-id="48aee-125">In the next unit, we'll adjust the data to make it meet our needs.</span></span> <span data-ttu-id="48aee-126">Procesu úprav připojených dat se říká *formování*.</span><span class="sxs-lookup"><span data-stu-id="48aee-126">The process of adjusting connected data is called *shaping*.</span></span>