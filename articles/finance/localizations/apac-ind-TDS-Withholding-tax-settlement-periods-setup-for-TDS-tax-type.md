---
title: إعداد فترات تسوية ضريبة الخصم لنوع ضريبة TDS
description: يوضح هذا الموضوع كيفية إعداد فترات التسوية لفترات تسوية الضريبة المخصومة في المصدر (TDS).
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 9430bc1386f127d02b598d6cad1b53f66e0cf2ba
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022985"
---
# <a name="set-up-withholding-tax-settlement-periods-for-the-tds-tax-type"></a><span data-ttu-id="b0319-103">إعداد فترات تسوية ضريبة الخصم لنوع ضريبة TDS</span><span class="sxs-lookup"><span data-stu-id="b0319-103">Set up withholding tax settlement periods for the TDS tax type</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b0319-104">يوضح هذا الموضوع كيفية إعداد فترات التسوية لفترات تسوية الضريبة المخصومة في المصدر (TDS).</span><span class="sxs-lookup"><span data-stu-id="b0319-104">This topic explains how to set up settlement periods for Tax Deducted at Source (TDS) settlement periods.</span></span>

1. <span data-ttu-id="b0319-105">انتقل إلى **الضريبة \> ضرائب غير مباشرة \> ضريبة الخصم \> فترات تسوية ضريبة الخصم**.</span><span class="sxs-lookup"><span data-stu-id="b0319-105">Go to **Tax \> Indirect taxes \> Withholding tax \> Withholding tax settlement periods**.</span></span>

    <span data-ttu-id="b0319-106">[![صفحة فترات تسوية ضريبة الخصم](./media/apac-ind-TDS-13.png)](./media/apac-ind-TDS-13.png)</span><span class="sxs-lookup"><span data-stu-id="b0319-106">[![Withholding tax settlement periods page](./media/apac-ind-TDS-13.png)](./media/apac-ind-TDS-13.png)</span></span>

2. <span data-ttu-id="b0319-107">في الحقل **نوع الضريبة**، حدد **TDS** لإعداد فترات تسوية ضريبة الخصم لنوع ضريبة TDS.</span><span class="sxs-lookup"><span data-stu-id="b0319-107">In the **Tax type** field, select **TDS** to set up withholding tax settlement periods for the TDS tax type.</span></span>
3. <span data-ttu-id="b0319-108">حدد **جديد** لإنشاء بند.</span><span class="sxs-lookup"><span data-stu-id="b0319-108">Select **New** to create a line.</span></span>
4. <span data-ttu-id="b0319-109">في الحقل **فترة التسوية**، أدخل اسمًا لفترة تسوية TDS.</span><span class="sxs-lookup"><span data-stu-id="b0319-109">In the **Settlement period** field, enter a name for the TDS settlement period.</span></span>
5. <span data-ttu-id="b0319-110">في الحقل **الوصف**، أدخل وصفًا.</span><span class="sxs-lookup"><span data-stu-id="b0319-110">In the **Description** field, enter a description.</span></span>
6. <span data-ttu-id="b0319-111">في الحقل **هيئه ضريبة الخصم**، حدد هيئة TDS التي تقوم بتعريف فترة تسوية TDS بها.</span><span class="sxs-lookup"><span data-stu-id="b0319-111">In the **Withholding tax authority** field, select the TDS authority that you're defining the TDS settlement period for.</span></span>
7. <span data-ttu-id="b0319-112">في علامة التبويب السريعة **عام**، في الحقل **الفترة الزمنية**، حدد نوع الفترة الزمنية لفترة تسوية TDS.</span><span class="sxs-lookup"><span data-stu-id="b0319-112">On the **General** FastTab, in the **Period interval** field, select the type of period interval for the TDS settlement period.</span></span>
8. <span data-ttu-id="b0319-113">في الحقل **عدد الوحدات**، حدد عدد الوحدات لنوع الفترة الزمنية.</span><span class="sxs-lookup"><span data-stu-id="b0319-113">In the **Number of units** field, specify the number of units for the period interval type.</span></span>
9. <span data-ttu-id="b0319-114">في علامة التبويب السريعة **الفترات**، في الحقل **من تاريخ**، حدد تاريخ البدء لفترة تسوية TDS.</span><span class="sxs-lookup"><span data-stu-id="b0319-114">On the **Periods** FastTab, in the **From date** field, select the start date for the TDS settlement period.</span></span> <span data-ttu-id="b0319-115">في الحقل **إلى التاريخ**، حدد تاريخ الانتهاء.</span><span class="sxs-lookup"><span data-stu-id="b0319-115">In the **To date** field, select the end date.</span></span>
10. <span data-ttu-id="b0319-116">لإنشاء فترة تسوية TDS لاحقة لفترة موجودة، استنادًا إلى الفترة الزمنية ووحدات الفترة، حدد **فترة جديدة**.</span><span class="sxs-lookup"><span data-stu-id="b0319-116">To create a subsequent TDS settlement period for an existing period, based on the period interval and period units, select **New period**.</span></span>
11. <span data-ttu-id="b0319-117">لعرض تفاصيل تسوية TDS الدورية التي يتم تشغيلها لفترة تسوية معينة، حدد **مدفوعات ضريبة الخصم** لفتح الصفحة **دفع ضريبة الخصم**.</span><span class="sxs-lookup"><span data-stu-id="b0319-117">To view the details of the periodic TDS settlement that is run for a specific settlement period, select **Withholding tax payments** to open the **Withholding tax payment** page.</span></span>

    > [!NOTE]
    > <span data-ttu-id="b0319-118">لتشغيل عملية تسوية TDS الدورية، انتقل إلى **دفتر الأستاذ العام \> دوري \> ضريبة الخصم \> دفع ضريبة الخصم**.</span><span class="sxs-lookup"><span data-stu-id="b0319-118">To run the periodic TDS settlement process, go to **General ledger \> Periodic \> Withholding tax \> Withholding tax payment**.</span></span>

    <span data-ttu-id="b0319-119">[![صفحة دفعة ضريبة الخصم](./media/apac-ind-TDS-15.png)](./media/apac-ind-TDS-15.png)</span><span class="sxs-lookup"><span data-stu-id="b0319-119">[![Withholding tax payment page](./media/apac-ind-TDS-15.png)](./media/apac-ind-TDS-15.png)</span></span>

12. <span data-ttu-id="b0319-120">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="b0319-120">Close the page.</span></span>
