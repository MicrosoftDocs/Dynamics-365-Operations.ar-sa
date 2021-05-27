---
title: إعداد مجموعة TDS وPAN ومعلومات TAN للموردين والعملاء
description: يوضح هذا الموضوع كيفية إعداد المعلومات المتعلقة بمجموعة الضريبة المخصومة في مجموعة المصدر (TDS)، ورقم الحساب الدائم (PAN)، ورقم حساب الضريبة (TAN) للموردين والعملاء.
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
ms.openlocfilehash: fd33b1775afefed798f1e9bb7601f4112222c430
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022999"
---
# <a name="tds-group-pan-and-tan-information-setup-for-vendors-and-customers"></a><span data-ttu-id="0cc9e-103">إعداد مجموعة TDS وPAN ومعلومات TAN للموردين والعملاء</span><span class="sxs-lookup"><span data-stu-id="0cc9e-103">TDS group, PAN, and TAN information setup for vendors and customers</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0cc9e-104">يوضح هذا الموضوع كيفية إعداد المعلومات المتعلقة بمجموعة الضريبة المخصومة في مجموعة المصدر (TDS)، ورقم الحساب الدائم (PAN)، ورقم حساب الضريبة (TAN) للموردين والعملاء.</span><span class="sxs-lookup"><span data-stu-id="0cc9e-104">This topic explains how to set up information about the Tax Deducted at Source (TDS) group, permanent account number (PAN), and tax account number (TAN) for vendors and customers.</span></span>

1. <span data-ttu-id="0cc9e-105">انتقل إلى **الحسابات المدينة \> الموردين \> كافة الموردين** أو **الحسابات المدينة \> العملاء \> جميع العملاء**.</span><span class="sxs-lookup"><span data-stu-id="0cc9e-105">Go to **Accounts payable \> Vendors \> All vendors** or **Accounts receivable \> Customers \> All customers**.</span></span>

    <span data-ttu-id="0cc9e-106">[![صفحة كافة الموردين](./media/apac-ind-TDS-55.png)](./media/apac-ind-TDS-55.png)</span><span class="sxs-lookup"><span data-stu-id="0cc9e-106">[![All vendors page](./media/apac-ind-TDS-55.png)](./media/apac-ind-TDS-55.png)</span></span>

2. <span data-ttu-id="0cc9e-107">في جزء الإجراء، حدد **جديد** لإنشاء مورد أو عميل، وأدخل التفاصيل المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="0cc9e-107">On the Action Pane, select **New** to create a vendor or customer, and enter the required details.</span></span> <span data-ttu-id="0cc9e-108">أو بدلاً من ذلك، حدد موردًا أو عميلاً موجودًا.</span><span class="sxs-lookup"><span data-stu-id="0cc9e-108">Alternatively, select an existing vendor or customer.</span></span>
3. <span data-ttu-id="0cc9e-109">في علامة التبويب السريعة **الفاتورة والتسليم**، في القسم **ضريبة الخصم**، قم بتعيين الخيار **حساب ضريبة الخصم** إلى **نعم** لحساب ضريبة الخصم أو TDS أو الضريبة التي تم جمعها في المصدر (TCS) للمورد أو العميل.</span><span class="sxs-lookup"><span data-stu-id="0cc9e-109">On the **Invoice and delivery** FastTab, in the **Withholding tax** section, set the **Calculate withholding tax** option to **Yes** to calculate withholding tax, TDS, or Tax Collected at Source (TCS) for the vendor or customer.</span></span>
4. <span data-ttu-id="0cc9e-110">يتم حساب TDS لفاتورة الشراء استنادًا إلى مجموعة TDS الافتراضية التي يتم تحديدها للمورد أو العميل.</span><span class="sxs-lookup"><span data-stu-id="0cc9e-110">TDS for a purchase invoice is calculated based on the default TDS group that is defined for the vendor or customer.</span></span> <span data-ttu-id="0cc9e-111">في حقل **مجموعة TDS**، حدد مجموعة TDS الافتراضية.</span><span class="sxs-lookup"><span data-stu-id="0cc9e-111">In the **TDS group** field, select the default TDS group.</span></span>

    > [!NOTE]
    > <span data-ttu-id="0cc9e-112">عندما تقوم بتحديد مجموعة TDS في الحقل **مجموعة TDS**، فقد يصبح الحقلين **مجموعة ضريبة الخصم** و **مجموعة TCS** غير متاحين.</span><span class="sxs-lookup"><span data-stu-id="0cc9e-112">When you select a TDS group in the **TDS group** field, the **Withholding tax group** and **TCS group** fields become unavailable.</span></span>

5. <span data-ttu-id="0cc9e-113">في علامة التبويب السريعة **معلومات الضريبة**، في القسم **معلومات PAN**، في الحقل **الحالة**، حدد حالة رقم الحساب الدائم للمورد أو العميل:</span><span class="sxs-lookup"><span data-stu-id="0cc9e-113">On the **Tax information** FastTab, in the **PAN information** section, in the **Status** field, select the status of the permanent account number for the vendor or customer:</span></span>

    - <span data-ttu-id="0cc9e-114">**غير متاح** – لا يحتوي المورد أو العميل على PAN.</span><span class="sxs-lookup"><span data-stu-id="0cc9e-114">**Not available** – The vendor or customer doesn't have a PAN.</span></span>
    - <span data-ttu-id="0cc9e-115">**مستلم**– يكون للمورد أو العميل PAN.</span><span class="sxs-lookup"><span data-stu-id="0cc9e-115">**Received** – The vendor or customer has a PAN.</span></span>
    - <span data-ttu-id="0cc9e-116">**مطبق** – تم تطبيق المورد أو العميل لـ PAN.</span><span class="sxs-lookup"><span data-stu-id="0cc9e-116">**Applied** – The vendor or customer has applied for a PAN.</span></span>
    - <span data-ttu-id="0cc9e-117">**غير صالح** – يمتلك المورد أو العميل PAN، ولكنه غير صالح.</span><span class="sxs-lookup"><span data-stu-id="0cc9e-117">**Invalid** – The vendor or customer has a PAN, but it isn't valid.</span></span>

6. <span data-ttu-id="0cc9e-118">إذا قمت بتحديد **مستلم** في الحقل **الحالة** للإشارة إلى أن المورد أو العميل له رقم PAN، أدخل PAN في الحقل **الرقم**.</span><span class="sxs-lookup"><span data-stu-id="0cc9e-118">If you selected **Received** in the **Status** field to indicate that the vendor or customer has a PAN, enter the PAN in the **Number** field.</span></span> <span data-ttu-id="0cc9e-119">يجب أن تتكون القيمة PAN من خمسة أحرف أبجدية، ثم أربعة أحرف رقمية، ثم حرفًا أبجديًا واحدًا.</span><span class="sxs-lookup"><span data-stu-id="0cc9e-119">The PAN must consist of five alphabetic characters, then four numeric characters, and then one alphabetic character.</span></span> <span data-ttu-id="0cc9e-120">وفيما يلي مثال على ذلك: **ABCDE1260A**.</span><span class="sxs-lookup"><span data-stu-id="0cc9e-120">Here is an example: **ABCDE1260A**.</span></span>
7. <span data-ttu-id="0cc9e-121">إذا قمت بتحديد **مطبق** في الحقل **الحالة** للإشارة إلى أن المورد أو العميل قد قام بتطبيق رقم PAN، أدخل الرقم المرجعي في الحقل **الرقم المرجعي**.</span><span class="sxs-lookup"><span data-stu-id="0cc9e-121">If you selected **Applied** in the **Status** field to indicate that the vendor or customer has applied for PAN, enter the reference number in the **Reference number** field.</span></span>
8. <span data-ttu-id="0cc9e-122">في الحقل **طبيعة المقيم**، حدد فئة طبيعة المقيم التي ينتمي إليها المورد أو العميل:</span><span class="sxs-lookup"><span data-stu-id="0cc9e-122">In the **Nature of assessee** field, select the nature of assessee category that the vendor or customer belongs to:</span></span>

    - <span data-ttu-id="0cc9e-123">الشركة</span><span class="sxs-lookup"><span data-stu-id="0cc9e-123">Company</span></span>
    - <span data-ttu-id="0cc9e-124">HUF</span><span class="sxs-lookup"><span data-stu-id="0cc9e-124">HUF</span></span>
    - <span data-ttu-id="0cc9e-125">تأكيد</span><span class="sxs-lookup"><span data-stu-id="0cc9e-125">Firm</span></span>
    - <span data-ttu-id="0cc9e-126">فردي</span><span class="sxs-lookup"><span data-stu-id="0cc9e-126">Individual</span></span>
    - <span data-ttu-id="0cc9e-127">AOP</span><span class="sxs-lookup"><span data-stu-id="0cc9e-127">AOP</span></span>
    - <span data-ttu-id="0cc9e-128">BOI</span><span class="sxs-lookup"><span data-stu-id="0cc9e-128">BOI</span></span>
    - <span data-ttu-id="0cc9e-129">السلطة المحلية</span><span class="sxs-lookup"><span data-stu-id="0cc9e-129">Local authority</span></span>
    - <span data-ttu-id="0cc9e-130">غير ذلك</span><span class="sxs-lookup"><span data-stu-id="0cc9e-130">Others</span></span>

    <span data-ttu-id="0cc9e-131">[![علامة التبويب السريعة معلومات الضريبة](./media/apac-ind-TDS-56.png)](./media/apac-ind-TDS-56.png)</span><span class="sxs-lookup"><span data-stu-id="0cc9e-131">[![Tax information FastTab](./media/apac-ind-TDS-56.png)](./media/apac-ind-TDS-56.png)</span></span>

9. <span data-ttu-id="0cc9e-132">في جزء الإجراءات، ضمن علامة التبويب **المورد**، في مجموعة **التسجيل**، حدد **معرفات التسجيل** لفتح الصفحة **إدارة العناوين**.</span><span class="sxs-lookup"><span data-stu-id="0cc9e-132">On the Action Pane, on the **Vendor** tab, in the **Registration** group, select **Registration IDs** to open the **Manage addresses** page.</span></span>
10. <span data-ttu-id="0cc9e-133">في الصفحة **إدارة العناوين**، في علامة التبويب السريعة **معلومات الضريبة**، حدد **إضافة** أو **تحرير** لفتح الصفحة **إدارة معلومات الضريبة**، حيث يمكنك الاحتفاظ بإدخال تسجيل الضريبة.</span><span class="sxs-lookup"><span data-stu-id="0cc9e-133">On the **Manage addresses** page, on the **Tax information** FastTab, select **Add** or **Edit** to open the **Manage tax information** page, where you can maintain the tax registration entry.</span></span>
11. <span data-ttu-id="0cc9e-134">في الصفحة **إدارة معلومات الضريبة**، على علامة التبويب السريعة **ضريبة الخصم**، في الحقل **رقم حساب الضريبة (TAN)**، أدخل الرقم TAN.</span><span class="sxs-lookup"><span data-stu-id="0cc9e-134">On the **Manage tax information** page, on the **Withholding tax** FastTab, in the **Tax Account Number (TAN)** field, enter the TAN.</span></span> <span data-ttu-id="0cc9e-135">يجب أن تتكون القيمة TAN من أربعة أحرف أبجدية، ثم خمسة أحرف رقمية، ثم حرفًا أبجديًا واحدًا.</span><span class="sxs-lookup"><span data-stu-id="0cc9e-135">The TAN must consist of four alphabetic characters, then five numeric characters, and then one alphabetic character.</span></span> <span data-ttu-id="0cc9e-136">وفيما يلي مثال على ذلك: **AFGH54821T**.</span><span class="sxs-lookup"><span data-stu-id="0cc9e-136">Here is an example: **AFGH54821T**.</span></span>
12. <span data-ttu-id="0cc9e-137">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="0cc9e-137">Close the page.</span></span>
