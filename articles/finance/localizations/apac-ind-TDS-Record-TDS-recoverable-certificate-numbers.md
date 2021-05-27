---
title: قم بتسجيل أرقام شهادات تخويل TDS قابلة للاسترداد
description: يوضح هذا الموضوع كيفية استخدام الصفحة الشهادات القابلة للاسترداد لتسجيل أرقام الشهادات وتواريخها لشهادات الضريبة المخصومة في المصدر (TDS) التي يتم استلامها لمورد أو عميل أو دفتر أستاذ معين.
author: kailiang
mms.date: 02/12/2021
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
ms.openlocfilehash: b501c331cccc6d030f36d0a13ba0a6a13c08c733
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022984"
---
# <a name="record-tds-recoverable-certificate-numbers"></a><span data-ttu-id="354ca-103">قم بتسجيل أرقام شهادات تخويل TDS قابلة للاسترداد</span><span class="sxs-lookup"><span data-stu-id="354ca-103">Record TDS recoverable certificate numbers</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="354ca-104">يوضح هذا الموضوع كيفية استخدام الصفحة **الشهادات القابلة للاسترداد** لتسجيل أرقام الشهادات وتواريخها لشهادات الضريبة المخصومة في المصدر (TDS) التي يتم استلامها لمورد أو عميل أو دفتر أستاذ معين.</span><span class="sxs-lookup"><span data-stu-id="354ca-104">This topic explains how to use the **Recoverable certificates** page to record the certificate numbers and dates for Tax Deducted at Source (TDS) certificates that are received for a specific vendor, customer, or ledger.</span></span> <span data-ttu-id="354ca-105">لتحديث أرقام شهادات TDS وتواريخها التي يتم تسجيلها لحركات TDS في هذه الصفحة، استخدم الصفحة **تحديث الشهادة** (**دفتر الأستاذ العام \> دوري \> ضريبة الخصم \> تحديث الشهادة**).</span><span class="sxs-lookup"><span data-stu-id="354ca-105">To update the TDS certificate numbers and dates that are recorded for TDS transactions on this page, use the **Update certificate** page (**General ledger \> Periodic \> Withholding tax \> Update certificate**).</span></span> <span data-ttu-id="354ca-106">بعد الانتهاء من تحديث أرقام الشهادات TDS، قم بإغلاقها.</span><span class="sxs-lookup"><span data-stu-id="354ca-106">After you've finished updating TDS certificate numbers, close them.</span></span>

<span data-ttu-id="354ca-107">اتبع هذه الخطوات لتسجيل وأرقام شهادات TDS وتواريخها.</span><span class="sxs-lookup"><span data-stu-id="354ca-107">Follow these steps to record the TDS certificate numbers and dates.</span></span>

1. <span data-ttu-id="354ca-108">انتقل إلى **ضريبة \> ضريبة غير مباشرة \> ضريبة خصم \> شهادات قابلة للاسترداد**.</span><span class="sxs-lookup"><span data-stu-id="354ca-108">Go to **Tax \> Indirect tax \> Withholding tax \> Recoverable certificates**.</span></span>

    <span data-ttu-id="354ca-109">[![صفحة الشهادات القابلة للاسترداد](./media/apac-ind-TDS-49.png)](./media/apac-ind-TDS-49.png)</span><span class="sxs-lookup"><span data-stu-id="354ca-109">[![Recoverable certificates page](./media/apac-ind-TDS-49.png)](./media/apac-ind-TDS-49.png)</span></span> 

2. <span data-ttu-id="354ca-110">في الصفحة **الشهادات القابلة للاسترداد**، في الحقل **نوع الضريبة**، حدد **TDS**.</span><span class="sxs-lookup"><span data-stu-id="354ca-110">On the **Recoverable certificates** page, in the **Tax type** field, select **TDS**.</span></span>
3. <span data-ttu-id="354ca-111">حدد **جديد** لإنشاء سجل.</span><span class="sxs-lookup"><span data-stu-id="354ca-111">Select **New** to create a record.</span></span>
4. <span data-ttu-id="354ca-112">في الحقل **رقم الشهادة**، أدخل رقم شهادة TDS.</span><span class="sxs-lookup"><span data-stu-id="354ca-112">In the **Certificate number** field, enter the TDS certificate number.</span></span>
5. <span data-ttu-id="354ca-113">في الحقل **نوع الحساب**، حدد نوع الحساب الذي يتم استلام شهادة TDS له: **المورد** أو **العميل** أو **دفتر الأستاذ**.</span><span class="sxs-lookup"><span data-stu-id="354ca-113">In the **Account type** field, select the type of account that the TDS certificate is received for: **Vendor**, **Customer**, or **Ledger**.</span></span>
6. <span data-ttu-id="354ca-114">في الحقل **الحساب**، حدد رقم حساب المورد أو العميل أو دفتر الأستاذ، وفقًا لنوع الحساب الذي قمت بتحديده.</span><span class="sxs-lookup"><span data-stu-id="354ca-114">In the **Account** field, select the vendor, customer, or ledger account number, depending on the account type that you selected.</span></span> <span data-ttu-id="354ca-115">يظهر الحقل **الاسم** اسم المورد أو العميل أو حساب دفتر الأستاذ.</span><span class="sxs-lookup"><span data-stu-id="354ca-115">The **Name** field shows the name of the vendor, customer, or ledger account.</span></span>
7. <span data-ttu-id="354ca-116">في الحقل **مبلغ الشهادة**، أدخل مبلغ الشهادة الرقمية.</span><span class="sxs-lookup"><span data-stu-id="354ca-116">In the **Certificate amount** field, enter the amount of the TDS certificate.</span></span>
8. <span data-ttu-id="354ca-117">في الحقل **التاريخ**، أدخل تاريخ الشهادة لرقم الشهادة.</span><span class="sxs-lookup"><span data-stu-id="354ca-117">In the **Date** field, enter the certificate date for the certificate number.</span></span>
9. <span data-ttu-id="354ca-118">حدد **الاستعلامات** لفتح الصفحة **حركات الشهادة**، حيث يمكنك عرض الحركات TDS التي يتم فيها تحديث رقم الشهادة TDS والتاريخ الخاص به.</span><span class="sxs-lookup"><span data-stu-id="354ca-118">Select **Inquiries** to open the **Certificate transactions** page, where you can view the TDS transactions that the TDS certificate number and date are updated for.</span></span> <span data-ttu-id="354ca-119">يمكن تحديث هذه المعلومات في الصفحة **تحديث الشهادات** (**الضريبة \> الإقرارات \> ضريبة الخصم \> تحديث الشهادة**).</span><span class="sxs-lookup"><span data-stu-id="354ca-119">This information can be updated on the **Update certificate** page (**Tax \> Declarations \> Withholding tax \> Update certificate**).</span></span>

    <span data-ttu-id="354ca-120">تعرض الصفحة **تحديث الشهادة** المعلومات التالية لكل حركة TDS:</span><span class="sxs-lookup"><span data-stu-id="354ca-120">The **Update certificate** page shows the following information for each TDS transaction:</span></span>

    - <span data-ttu-id="354ca-121">**التاريخ** – تاريخ الترحيل الخاص بحركة TDS.</span><span class="sxs-lookup"><span data-stu-id="354ca-121">**Date** – The posting date of the TDS transaction.</span></span>
    - <span data-ttu-id="354ca-122">**الإيصال** – رقم إيصال حركة TDS.</span><span class="sxs-lookup"><span data-stu-id="354ca-122">**Voucher** – The voucher number of the TDS transaction.</span></span>
    - <span data-ttu-id="354ca-123">**المصدر** – الوحدة النمطية التي يتم إنشاء حركة TDS إليها.</span><span class="sxs-lookup"><span data-stu-id="354ca-123">**Source** – The module that the TDS transaction was created in.</span></span>
    - <span data-ttu-id="354ca-124">**الحساب** – رقم حساب المورد أو العميل أو دفتر الأستاذ الذي تم إنشاء حركة TDS له.</span><span class="sxs-lookup"><span data-stu-id="354ca-124">**Account** – The vendor, customer, or ledger account number that the TDS transaction was created for.</span></span>
    - <span data-ttu-id="354ca-125">**الاسم** – رقم حساب المورد أو العميل أو دفتر الأستاذ الذي تم إنشاء حركة TDS له.</span><span class="sxs-lookup"><span data-stu-id="354ca-125">**Name** – The name of the vendor, customer, or ledger account that the TDS transaction was created for.</span></span>
    - <span data-ttu-id="354ca-126">**المبلغ** – مبلغ الفاتورة الذي يتم حساب TDS به.</span><span class="sxs-lookup"><span data-stu-id="354ca-126">**Amount** – The invoice amount that the TDS was calculated on.</span></span>
    - <span data-ttu-id="354ca-127">**مبلغ الضريبة** – مبلغ ضريبة TDS الذي تم حسابه للحركة.</span><span class="sxs-lookup"><span data-stu-id="354ca-127">**Tax amount** – The TDS tax amount that was calculated for the transaction.</span></span>
    - <span data-ttu-id="354ca-128">**تاريخ الشهادة** – تاريخ شهادة TDS الذي يتم تحديثه لحركة TDS.</span><span class="sxs-lookup"><span data-stu-id="354ca-128">**Certificate date** – The TDS certificate date that was updated for the TDS transaction.</span></span>
    - <span data-ttu-id="354ca-129">**رقم الشهادة** – رقم شهادة TDS الذي يتم تحديثه لحركة TDS.</span><span class="sxs-lookup"><span data-stu-id="354ca-129">**Certificate number** – TDS certificate number that was updated for the TDS transaction.</span></span>

10. <span data-ttu-id="354ca-130">في الصفحة **الشهادات القابلة للاسترداد**، حدد خانة الاختيار **مغلق** لإغلاق رقم الشهادة TDS بعد الانتهاء من تحديثه لحركات TDS في الصفحة **تحديث الشهادة**.</span><span class="sxs-lookup"><span data-stu-id="354ca-130">On the **Recoverable certificates** page, select the **Closed** check box to close the TDS certificate number after you've finished updating it for TDS transactions on the **Update certificate** page.</span></span>

    <span data-ttu-id="354ca-131">لتحديد خانة الاختيار **مغلق** لكافة السجلات في الصفحة، حدد **وضع علامة الكل**.</span><span class="sxs-lookup"><span data-stu-id="354ca-131">To select the **Closed** check box for all records on the page, select **Mark all**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="354ca-132">ولا تتوفر أرقام شهادات TDS التي يتم تحديد خانة الاختيار **مغلق** لها في الصفحة **تحديث الشهادة**.</span><span class="sxs-lookup"><span data-stu-id="354ca-132">TDS certificate numbers that the **Closed** check box is selected for aren't available on the **Update certificate** page.</span></span>
