---
ms.openlocfilehash: 2cb3fb64062e9d889fb26da5e7787ee9bd7870b3
ms.sourcegitcommit: d4531d76c2cc5030d9fd2c39f3c6c73ce8768841
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/26/2019
ms.locfileid: "58473966"
---
<span data-ttu-id="268c9-101">V této lekci vytvoříte entitu a pak upravíte klíčové komponenty, jako jsou pole, relace, zobrazení a formuláře.</span><span class="sxs-lookup"><span data-stu-id="268c9-101">In this unit, you'll create an entity and then customize key components, like fields, relationships, views, and forms.</span></span> <span data-ttu-id="268c9-102">Dozvíte se, jak provést tyto akce:</span><span class="sxs-lookup"><span data-stu-id="268c9-102">You'll learn how to:</span></span>

- <span data-ttu-id="268c9-103">Vytvoření vlastní entity</span><span class="sxs-lookup"><span data-stu-id="268c9-103">Create a custom entity.</span></span>
- <span data-ttu-id="268c9-104">Přidání vlastních polí do entity</span><span class="sxs-lookup"><span data-stu-id="268c9-104">Add custom fields to your entity.</span></span>
- <span data-ttu-id="268c9-105">Přidání relace entity</span><span class="sxs-lookup"><span data-stu-id="268c9-105">Add an entity relationship.</span></span>
- <span data-ttu-id="268c9-106">Přizpůsobení zobrazení</span><span class="sxs-lookup"><span data-stu-id="268c9-106">Customize a view.</span></span>
- <span data-ttu-id="268c9-107">Přizpůsobení formuláře</span><span class="sxs-lookup"><span data-stu-id="268c9-107">Customize a form.</span></span>

<span data-ttu-id="268c9-108">Tento kurz sleduje společnost Contoso, která se zabývá péčí o domácí mazlíčky a věnuje se úpravám zevnějšku psů a koček.</span><span class="sxs-lookup"><span data-stu-id="268c9-108">The tutorial follows the Contoso company, which is a pet grooming business that grooms dogs and cats.</span></span> <span data-ttu-id="268c9-109">Contoso potřebuje aplikaci pro sledování klientů a domácích mazlíčků, kterou můžou využívat zaměstnanci na různých zařízeních.</span><span class="sxs-lookup"><span data-stu-id="268c9-109">Contoso needs an app for client and pet tracking that can be used by employees on a variety of devices.</span></span>

## <a name="create-a-custom-entity"></a><span data-ttu-id="268c9-110">Vytvoření vlastní entity</span><span class="sxs-lookup"><span data-stu-id="268c9-110">Create a custom entity</span></span>

1. <span data-ttu-id="268c9-111">V levém navigačním podokně rozbalte **Data**, vyberte **Entity** a pak vyberte **Nová entita**.</span><span class="sxs-lookup"><span data-stu-id="268c9-111">In the left navigation pane, expand **Data**, select **Entities**, and then select **New entity**.</span></span>

2. <span data-ttu-id="268c9-112">Zadejte tyto hodnoty:</span><span class="sxs-lookup"><span data-stu-id="268c9-112">Enter the following values:</span></span>

    - <span data-ttu-id="268c9-113">**Zobrazovaný název:** *Domácí mazlíček*</span><span class="sxs-lookup"><span data-stu-id="268c9-113">**Display name**: *Pet*</span></span>
    - <span data-ttu-id="268c9-114">**Popis:** *Vlastní entita sloužící ke sledování služeb pro domácí mazlíčky*</span><span class="sxs-lookup"><span data-stu-id="268c9-114">**Description**: *Custom entity to track pet services*</span></span>

3. <span data-ttu-id="268c9-115">Vyberte **Další** a pak po zobrazení výchozích polí vyberte **Uložit entitu**.</span><span class="sxs-lookup"><span data-stu-id="268c9-115">Select **Next**, and then, after the default fields are shown, select **Save Entity**.</span></span>

## <a name="add-and-customize-fields"></a><span data-ttu-id="268c9-116">Přidání a přizpůsobení polí</span><span class="sxs-lookup"><span data-stu-id="268c9-116">Add and customize fields</span></span>

1. <span data-ttu-id="268c9-117">V seznamu entit vyberte entitu **Domácí mazlíček**, kterou jste vytvořili v předchozí části.</span><span class="sxs-lookup"><span data-stu-id="268c9-117">In the list of entities, select the **Pet** entity that you created in the previous section.</span></span>
2. <span data-ttu-id="268c9-118">Na kartě **Pole** vyberte pole **Domácí mazlíček**.</span><span class="sxs-lookup"><span data-stu-id="268c9-118">On the **Fields** tab, select the **Pet** field.</span></span>
3. <span data-ttu-id="268c9-119">V pravém podokně proveďte následující změny pole **Zobrazovaný název**:</span><span class="sxs-lookup"><span data-stu-id="268c9-119">In the right pane, make the following changes to the **Display name** field:</span></span>

    - <span data-ttu-id="268c9-120">Změňte hodnotu **Zobrazovaný název** z hodnoty *Domácí mazlíček* na *Jméno domácího mazlíčka*.</span><span class="sxs-lookup"><span data-stu-id="268c9-120">Change the **Display name** value from *Pet* to *Pet Name*.</span></span>
    - <span data-ttu-id="268c9-121">Vyberte **Prohledávatelné**.</span><span class="sxs-lookup"><span data-stu-id="268c9-121">Select **Searchable**.</span></span>

    > ![Změna primárního pole](../media/primary-field.png)

3. <span data-ttu-id="268c9-123">Vyberte **Hotovo**.</span><span class="sxs-lookup"><span data-stu-id="268c9-123">Select **Done**.</span></span>
4. <span data-ttu-id="268c9-124">Na kartě **Pole** na panelu nástrojů návrháře entit vyberte **Přidat pole**.</span><span class="sxs-lookup"><span data-stu-id="268c9-124">On the **Fields** tab, on the entity designer toolbar, select **Add field**.</span></span>
5. <span data-ttu-id="268c9-125">V podokně **Vlastnosti pole** zadejte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="268c9-125">In the **Field properties** pane, enter the following values:</span></span>

    - <span data-ttu-id="268c9-126">**Zobrazovaný název:** *Druh*</span><span class="sxs-lookup"><span data-stu-id="268c9-126">**Display name**: *Species*</span></span>
    - <span data-ttu-id="268c9-127">**Datový typ:** *Sada možností*</span><span class="sxs-lookup"><span data-stu-id="268c9-127">**Data type**: *Option Set*</span></span>
    - <span data-ttu-id="268c9-128">**Sada možností:** *Nová sada možností*</span><span class="sxs-lookup"><span data-stu-id="268c9-128">**Option set**: *New option set*</span></span>

6. <span data-ttu-id="268c9-129">Vytvoření sady možností:</span><span class="sxs-lookup"><span data-stu-id="268c9-129">Create the option set:</span></span>

    1. <span data-ttu-id="268c9-130">Vyberte **Přidat novou položku**.</span><span class="sxs-lookup"><span data-stu-id="268c9-130">Select **Add new item**.</span></span>
    2. <span data-ttu-id="268c9-131">Nahraďte *Nová možnost* hodnotou *Pes*.</span><span class="sxs-lookup"><span data-stu-id="268c9-131">Replace *New option* with *Dog*.</span></span>
    3. <span data-ttu-id="268c9-132">Vyberte **Přidat novou položku**.</span><span class="sxs-lookup"><span data-stu-id="268c9-132">Select **Add new item**.</span></span>
    4. <span data-ttu-id="268c9-133">Nahraďte *Nová možnost* hodnotou *Kočka*.</span><span class="sxs-lookup"><span data-stu-id="268c9-133">Replace *New option* with *Cat*.</span></span>
    5. <span data-ttu-id="268c9-134">Vyberte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="268c9-134">Select **Save**.</span></span>

    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="268c9-135">![Nová sada možností](../media/optionset-add-items.png)</span><span class="sxs-lookup"><span data-stu-id="268c9-135">![New option set](../media/optionset-add-items.png)</span></span>

7. <span data-ttu-id="268c9-136">Vyberte **Prohledávatelné** a pak vyberte **Hotovo**.</span><span class="sxs-lookup"><span data-stu-id="268c9-136">Select **Searchable**, and then select **Done**.</span></span>
8. <span data-ttu-id="268c9-137">Na panelu nástrojů návrháře entit vyberte **Přidat pole**.</span><span class="sxs-lookup"><span data-stu-id="268c9-137">On the entity designer toolbar, select **Add field**.</span></span>
9. <span data-ttu-id="268c9-138">V podokně **Vlastnosti pole** zadejte následující hodnoty a pak vyberte **Hotovo**:</span><span class="sxs-lookup"><span data-stu-id="268c9-138">In the **Field properties** pane, enter the following values, and then select **Done**:</span></span>

    - <span data-ttu-id="268c9-139">**Zobrazovaný název:** *Plemeno*</span><span class="sxs-lookup"><span data-stu-id="268c9-139">**Display name**: *Breed*</span></span>
    - <span data-ttu-id="268c9-140">**Datový typ:** *Text*</span><span class="sxs-lookup"><span data-stu-id="268c9-140">**Data type**: *Text*</span></span>
    - <span data-ttu-id="268c9-141">**Prohledávatelné:** *Ano*</span><span class="sxs-lookup"><span data-stu-id="268c9-141">**Searchable**: *Yes*</span></span>

10. <span data-ttu-id="268c9-142">Na panelu nástrojů návrháře entit vyberte **Přidat pole**.</span><span class="sxs-lookup"><span data-stu-id="268c9-142">On the entity designer toolbar, select **Add field**.</span></span>
11. <span data-ttu-id="268c9-143">V podokně **Vlastnosti pole** zadejte následující hodnoty a pak vyberte **Hotovo**:</span><span class="sxs-lookup"><span data-stu-id="268c9-143">In the **Field properties** pane, enter the following values, and then select **Done**:</span></span>

    - <span data-ttu-id="268c9-144">**Zobrazovaný název:** *Datum návštěvy*</span><span class="sxs-lookup"><span data-stu-id="268c9-144">**Display name**: *Appointment date*</span></span>
    - <span data-ttu-id="268c9-145">**Datový typ:** *Datum a čas*</span><span class="sxs-lookup"><span data-stu-id="268c9-145">**Data type**: *Date and time*</span></span>

12. <span data-ttu-id="268c9-146">Vyberte **Uložit entitu**.</span><span class="sxs-lookup"><span data-stu-id="268c9-146">Select **Save Entity**.</span></span>

## <a name="add-a-relationship"></a><span data-ttu-id="268c9-147">Přidání relace</span><span class="sxs-lookup"><span data-stu-id="268c9-147">Add a relationship</span></span>

1. <span data-ttu-id="268c9-148">Na kartě **Relace** na panelu nástrojů návrháře entit vyberte **Přidat relaci** a pak vyberte **N:1**.</span><span class="sxs-lookup"><span data-stu-id="268c9-148">On the **Relationships** tab, on the entity designer toolbar, select **Add relationship**, and then select **Many-to-one**.</span></span>
2. <span data-ttu-id="268c9-149">V pravém podokně v seznamu **Související** vyberte **Obchodní vztah**.</span><span class="sxs-lookup"><span data-stu-id="268c9-149">In the right pane, in the **Related** list, select **Account**.</span></span>
3. <span data-ttu-id="268c9-150">Vyberte **Hotovo**.</span><span class="sxs-lookup"><span data-stu-id="268c9-150">Select **Done**.</span></span>
4. <span data-ttu-id="268c9-151">Vyberte **Uložit entitu**.</span><span class="sxs-lookup"><span data-stu-id="268c9-151">Select **Save Entity**.</span></span>

    <span data-ttu-id="268c9-152">Všimněte si, že když přidáte relaci N:1, na kartu **Pole** se automaticky přidá pole **Účet** s datovým typem **Vyhledávání**.</span><span class="sxs-lookup"><span data-stu-id="268c9-152">Notice that when you add a many-to-one relationship, an **Account** field of the **Lookup** data type is automatically added to your list of fields on the **Fields** tab.</span></span>

    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="268c9-153">![Vyhledávací pole Účet](../media/account-lookup-field.png)</span><span class="sxs-lookup"><span data-stu-id="268c9-153">![Account lookup field](../media/account-lookup-field.png)</span></span>

## <a name="customize-a-view"></a><span data-ttu-id="268c9-154">Přizpůsobení zobrazení</span><span class="sxs-lookup"><span data-stu-id="268c9-154">Customize a view</span></span>

1. <span data-ttu-id="268c9-155">Na kartě **Zobrazení** vyberte **Aktivní domácí mazlíčci**.</span><span class="sxs-lookup"><span data-stu-id="268c9-155">On the **Views** tab, select the **Active Pets** view.</span></span> <span data-ttu-id="268c9-156">Pokud zobrazení **Aktivní domácí mazlíčci** není uvedené, vyberte **Odebrat filtr**.</span><span class="sxs-lookup"><span data-stu-id="268c9-156">If you don't see the **Active Pets** view, select **Remove filter**.</span></span>
2. <span data-ttu-id="268c9-157">V návrháři zobrazení vyberte **Přidat sloupce**, vyberte následující sloupce a pak vyberte **OK**:</span><span class="sxs-lookup"><span data-stu-id="268c9-157">In the view designer, select **Add Columns**, select the following columns, and then select **OK**:</span></span>

    - <span data-ttu-id="268c9-158">Účet</span><span class="sxs-lookup"><span data-stu-id="268c9-158">Account</span></span>
    - <span data-ttu-id="268c9-159">Datum návštěvy</span><span class="sxs-lookup"><span data-stu-id="268c9-159">Appointment date</span></span>
    - <span data-ttu-id="268c9-160">Plemeno</span><span class="sxs-lookup"><span data-stu-id="268c9-160">Breed</span></span>
    - <span data-ttu-id="268c9-161">Druh</span><span class="sxs-lookup"><span data-stu-id="268c9-161">Species</span></span>

3. <span data-ttu-id="268c9-162">Vyberte sloupec **Vytvořeno**, vyberte **Odebrat** a pak potvrďte odebrání sloupce výběrem **OK**.</span><span class="sxs-lookup"><span data-stu-id="268c9-162">Select the **Created On** column, select **Remove**, and then select **OK** to confirm the column removal.</span></span>
4. <span data-ttu-id="268c9-163">Pokud chcete sloupce uspořádat, vyberte sloupec, který chcete přesunout, a potom používejte tlačítka se šipkami (**\<-** a **-\>**), dokud zobrazení nevypadá takto.</span><span class="sxs-lookup"><span data-stu-id="268c9-163">To arrange the columns, select the column to move, and then use the arrow buttons (**\<-** and **-\>**) until your view looks like this.</span></span>

    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="268c9-164">![Zobrazení Aktivní domácí mazlíčci](../media/active-pets-view.png)</span><span class="sxs-lookup"><span data-stu-id="268c9-164">![Active pets view](../media/active-pets-view.png)</span></span>

5. <span data-ttu-id="268c9-165">Na panelu nástrojů návrháře zobrazení vyberte **Uložit a zavřít**.</span><span class="sxs-lookup"><span data-stu-id="268c9-165">On the view designer toolbar, select **Save and Close**.</span></span>

## <a name="customize-the-main-form"></a><span data-ttu-id="268c9-166">Přizpůsobení hlavního formuláře</span><span class="sxs-lookup"><span data-stu-id="268c9-166">Customize the main form</span></span>

1. <span data-ttu-id="268c9-167">V PowerApps vyberte v levém navigačním podokně **Modelem řízený**.</span><span class="sxs-lookup"><span data-stu-id="268c9-167">In PowerApps, in the left navigation pane, select **Model-driven**.</span></span>
2. <span data-ttu-id="268c9-168">V levém navigačním podokně rozbalte **Data**, vyberte **Entity** a pak vyberte **Domácí mazlíček**.</span><span class="sxs-lookup"><span data-stu-id="268c9-168">In the left navigation pane, expand **Data**, select **Entities**, and then select **Pet**.</span></span>
3. <span data-ttu-id="268c9-169">Na kartě **Formuláře** vyberte **Informace** vedle typu formuláře **Hlavní** a otevřete editor formulářů.</span><span class="sxs-lookup"><span data-stu-id="268c9-169">On the **Forms** tab, select **Information** next to the **Main** form type to open the form editor.</span></span>

    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="268c9-170">![Úprava hlavního formuláře](../media/main-form-edit.png)</span><span class="sxs-lookup"><span data-stu-id="268c9-170">![Edit main form](../media/main-form-edit.png)</span></span>

4. <span data-ttu-id="268c9-171">V editoru formulářů přetáhněte pole **Druh**, **Plemeno**, **Datum návštěvy** a **Účet** z podokna **Průzkumník polí** do části plátna formuláře **Obecné**, aby formulář vypadal takto.</span><span class="sxs-lookup"><span data-stu-id="268c9-171">In the form editor, drag the **Species**, **Breed**, **Appointment date**, and **Account** fields from the **Field Explorer** pane to the **General** section of the form canvas, so that the form looks like this.</span></span>

    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="268c9-172">![Výběr polí pro hlavní formulář](../media/main-form-edit2.png)</span><span class="sxs-lookup"><span data-stu-id="268c9-172">![Select fields for main form](../media/main-form-edit2.png)</span></span>

5. <span data-ttu-id="268c9-173">Vyberte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="268c9-173">Select **Save**.</span></span>
6. <span data-ttu-id="268c9-174">Vyberte **Publikovat**.</span><span class="sxs-lookup"><span data-stu-id="268c9-174">Select **Publish**.</span></span>
7. <span data-ttu-id="268c9-175">Výběrem **Uložit a zavřít** zavřete návrhář formulářů.</span><span class="sxs-lookup"><span data-stu-id="268c9-175">Select **Save and close** to close the form designer.</span></span>
