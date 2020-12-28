---
title: تخصيص رسوم المستندات البنكية لشحنة
description: يوضح هذا الموضوع كيف يمكن تخصيص المصاريف البنكية للمستند علي شحنه في أمر شراء.
author: v-oloski
manager: tfehr
ms.date: 11/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: ''
ms.search.scope: Core, Operations
ms.search.region: Saudi Arabia
ms.author: v-oloski
ms.search.validFrom: 2019-11-29
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 4b4f62dea839a996a1e8ac38fbf6762f0f47026e
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 11/25/2020
ms.locfileid: "4645879"
---
# <a name="allocate-bank-document-charges-to-a-shipment"></a><span data-ttu-id="691ae-103">تخصيص رسوم المستندات البنكية لشحنة</span><span class="sxs-lookup"><span data-stu-id="691ae-103">Allocate bank document charges to a shipment</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="691ae-104">يمكنك تخصيص مصاريف مستندات البنك التي يتم ترحيلها في دفتر اليومية العام إلى بنود أمر الشراء.</span><span class="sxs-lookup"><span data-stu-id="691ae-104">You can allocate bank document charges that are posted in the general journal to purchase order lines.</span></span> <span data-ttu-id="691ae-105">يجب ان يكون لأمر الشراء خطاب اعتماد أو مجموعه استيراد ذات صله.</span><span class="sxs-lookup"><span data-stu-id="691ae-105">The purchase order should have a related letter of credit or import collection.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="691ae-106">المتطلبات الأساسية</span><span class="sxs-lookup"><span data-stu-id="691ae-106">Prerequisites</span></span>

<span data-ttu-id="691ae-107">قبل البدء في تخصيص مصاريف مستندات البنك، [قم باعداد تسهيلات البنك وملفات تعريف الترحيل لخطابات الاعتماد](../cash-bank-management/tasks/set-up-bank-facilities-posting-profiles-letter-credit.md)، ثم قم بإنشاء أمر شراء يحتوي علي [خطاب اعتماد مستورد](https://docs.microsoft.com/dynamics365/finance/cash-bank-management/tasks/import-letter-credit).</span><span class="sxs-lookup"><span data-stu-id="691ae-107">Before you start to allocate the bank document charges, [set up bank facilities and posting profiles for letters of credit](../cash-bank-management/tasks/set-up-bank-facilities-posting-profiles-letter-credit.md), and create a purchase order that has an [imported letter of credit](https://docs.microsoft.com/dynamics365/finance/cash-bank-management/tasks/import-letter-credit).</span></span>

## <a name="set-up-a-charge-code-for-bank-document-charges"></a><span data-ttu-id="691ae-108">اعداد كود مصاريف لمصاريف مستندات البنك</span><span class="sxs-lookup"><span data-stu-id="691ae-108">Set up a charge code for bank document charges</span></span>

<span data-ttu-id="691ae-109">اتبع هذه الخطوات لاعداد كود مصاريف لمصاريف مستندات البنك.</span><span class="sxs-lookup"><span data-stu-id="691ae-109">Follow these steps to set up a charge code for bank document charges.</span></span>

1. <span data-ttu-id="691ae-110">انتقل إلى **الحسابات الدائنة** \> **إعداد** \> **إعداد المصاريف** \> **كود المصاريف**.</span><span class="sxs-lookup"><span data-stu-id="691ae-110">Go to **Accounts payable** \> **Setup** \> **Charges setup** \> **Charges code**.</span></span>
2. <span data-ttu-id="691ae-111">في علامة التبويب السريعة **الترحيل**، في قسم **المدين**، في الحقل **النوع**، حدد **صنف**.</span><span class="sxs-lookup"><span data-stu-id="691ae-111">On the **Posting** FastTab, in the **Debit** section, in the **Type** field, select **Item**.</span></span> <span data-ttu-id="691ae-112">يصبح خيار **كود مصاريف مستندات البنك** في قسم **رسوم المستندات البنكية** متاحا.</span><span class="sxs-lookup"><span data-stu-id="691ae-112">The **Bank document charge code** option in the **Bank document charge** section becomes available.</span></span>
3. <span data-ttu-id="691ae-113">قم بتعيين خيار **كود مصاريف مستندات البنك** إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="691ae-113">Set the **Bank document charge code** option to **Yes**.</span></span> <span data-ttu-id="691ae-114">ويتم تلقائيا تعيين حقل **النوع** في قسم **الائتمان** ولا يمكن تحريره.</span><span class="sxs-lookup"><span data-stu-id="691ae-114">The **Type** field in the **Credit** section is automatically set and can't be edited.</span></span>

![اعداد كود مصاريف لمصاريف مستندات البنك](media/apac-sau-bank-document-charge-setup.PNG)

## <a name="allocate-bank-document-charges"></a><span data-ttu-id="691ae-116">تخصيص رسوم المستندات البنكية</span><span class="sxs-lookup"><span data-stu-id="691ae-116">Allocate bank document charges</span></span>

<span data-ttu-id="691ae-117">اتبع الخطوات التالي لتخصيص رسوم المستندات البنكية.</span><span class="sxs-lookup"><span data-stu-id="691ae-117">Follow these steps to allocate bank document charges.</span></span>

1. <span data-ttu-id="691ae-118">قم بإنشاء أمر شراء يتضمن خطاب اعتماد أو مجموعه استيراد.</span><span class="sxs-lookup"><span data-stu-id="691ae-118">Create a purchase order that has a letter of credit or an import collection.</span></span> <span data-ttu-id="691ae-119">لمزيد من المعلومات، راجع [استيراد خطاب اعتماد](../cash-bank-management/tasks/import-letter-credit.md).</span><span class="sxs-lookup"><span data-stu-id="691ae-119">For more information, see [Import letter of credit](../cash-bank-management/tasks/import-letter-credit.md).</span></span>

    > [!NOTE]
    > <span data-ttu-id="691ae-120">يجب تاكيد خطاب الاعتماد أو تحصيل الاستيراد قبل ان تتمكن من تخصيص مصاريف مستندات البنك.</span><span class="sxs-lookup"><span data-stu-id="691ae-120">The letter of credit or import collection must be confirmed before you can allocate bank document charges.</span></span>

2. <span data-ttu-id="691ae-121">انتقل إلى **دفتر الأستاذ العام** \> **إدخالات دفتر اليومية** \> **دفاتر اليومية العامة‬**.</span><span class="sxs-lookup"><span data-stu-id="691ae-121">Go to **General ledger** \> **Journal entries** \> **General journals**.</span></span>
3. <span data-ttu-id="691ae-122">في جزء الإجراءات، حدد **البنود**.</span><span class="sxs-lookup"><span data-stu-id="691ae-122">On the Action Pane, select **Lines**.</span></span>
4. <span data-ttu-id="691ae-123">ضمن علامة التبويب **المدفوعات**، في القسم **خطاب الاعتماد/تحصيل الاستيراد**، قم بتعيين الحقول كما تحتاج.</span><span class="sxs-lookup"><span data-stu-id="691ae-123">On the **Payment** tab, in the **Letter of credit/import collection** section, set the fields as you require.</span></span>

    > [!NOTE]
    > <span data-ttu-id="691ae-124">يتم تعيين حقلي **نوع الحساب المقابل** و **الحساب المقابل** تلقائيا.</span><span class="sxs-lookup"><span data-stu-id="691ae-124">The **Offset account type** and **Offset account** fields are automatically set.</span></span>

    ![إدخال كود تكلفه مستند البنك في بند دفتر اليومية](media/apac-sau-general-journal-voucher.PNG)

5. <span data-ttu-id="691ae-126">في علامة التبويب **قائمه**، قم بتعيين حقلي **الحساب** و **مدين**.</span><span class="sxs-lookup"><span data-stu-id="691ae-126">On the **List** tab, set the **Account** and **Debit** fields.</span></span>
6. <span data-ttu-id="691ae-127">في الصفحة **خطاب الاعتماد/مجموعه الاستيراد**، في جزء الاجراء ، حدد **مستند البنك** \> **تكلفه مستند البنك**.</span><span class="sxs-lookup"><span data-stu-id="691ae-127">On the **Letter of credit/import collection** page, on the Action Pane, select **Bank document** \> **Bank document charge**.</span></span>

    ![تخصيص رسوم المستندات البنكية](media/apac-sau-allocate-bank-docment-charge.PNG)

    <span data-ttu-id="691ae-129">تم فتح خطاب الاعتماد أو تحصيل الاستيراد الذي قمت بإنشائه في أمر الشراء.</span><span class="sxs-lookup"><span data-stu-id="691ae-129">The letter of credit or import collection that you created in the purchase order is opened.</span></span> <span data-ttu-id="691ae-130">وينبغي ان يعرض رسوم المستندات البنكية التي تم ترحيلها في دفتر اليومية العام لخطاب الاعتماد هذا أو لتحصيل الاستيراد.</span><span class="sxs-lookup"><span data-stu-id="691ae-130">It should show the bank document charge that was posted in the general journal for this letter of credit or import collection.</span></span>

    ![حركات المستند البنكي الخاص بخطاب الاعتماد/تحصيل الاستيراد](media/apac-sau-lc-bank-document-transactions.PNG)

7. <span data-ttu-id="691ae-132">حدد حركه تكلفه المستند البنكي في وضع **التحرير**، ثم حدد **خطاب الاعتماد/تحصيل الاستيراد** لتخصيص تكلفه مستند البنك المحددة.</span><span class="sxs-lookup"><span data-stu-id="691ae-132">Select the bank document charge transaction in **Edit** mode, and then select **Letter of credit/import collection** to allocate the selected bank document charge.</span></span>

    > [!TIP]
    > <span data-ttu-id="691ae-133">يمكنك التحقق من صحة التوزيع عن طريق تحديد **حركات مصاريف الشحن** في علامة التبويب السريعة **البنود**.</span><span class="sxs-lookup"><span data-stu-id="691ae-133">You can validate the allocation by selecting **Shipment charge transactions** on the **Lines** FastTab.</span></span>

8. <span data-ttu-id="691ae-134">لتخصيص حركات مصاريف الشحن لبنود أمر الشراء ، في جزء الاجراء ، ضمن علامة التبويب **شراء**، في المجموعة **المصاريف**، حدد **الاحتفاظ بالمصاريف**، ثم حدد **توزيع**</span><span class="sxs-lookup"><span data-stu-id="691ae-134">To allocate shipment charge transactions to the purchase order lines, on the Action Pane, on the **Purchase** tab, in the **Charges** group, select **Maintain charges**, and then select **Allocate**.</span></span> <span data-ttu-id="691ae-135">يجب ان تظهر مصاريف المستندات البنكية التي قمت بتخصيصها لخطابات الاعتماد أو بنود تحصيل الاستيراد في القائمة.</span><span class="sxs-lookup"><span data-stu-id="691ae-135">The bank document charge that you allocated to letter of credit or import collection lines should appear in the list.</span></span>