---
title: إعداد سعر الفائدة المرتبط بمؤشر
description: يصف هذا الموضوع كيفية إعداد أسعار الفائدة المرتبطة بمؤشر . تكون أسعار الفائدة المرتبطة بمؤشر مطلوبة إذا كانت مؤسستك تقوم بربط مبالغ دفعات الإيجار بمجموعة من أسعار الفائدة المرتبطة بمؤشر.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: b6d201329996f23d94c0fc76a9635d3bb99c931e
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5249667"
---
# <a name="set-up-index-rates"></a><span data-ttu-id="7032c-104">إعداد سعر الفائدة المرتبط بمؤشر</span><span class="sxs-lookup"><span data-stu-id="7032c-104">Set up index rates</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7032c-105">إذا كانت دفعات الإيجار تعتمد على مؤشر ما، فيمكن إضافة أنواع سعر الفائدة المرتبط بمؤشر والاحتفاظ بها في النظام.</span><span class="sxs-lookup"><span data-stu-id="7032c-105">If lease payments depend on an index, the index rate types can be added and maintained in the system.</span></span> <span data-ttu-id="7032c-106">لإعادة تقييم دفعات الإيجار من الصفحة **نوع سعر الفائدة المرتبط بمؤشر**، تعمل عملية إعادة تقييم سعر الفائدة المرتبط بمؤشر على استخدام سعر الفائدة المرتبط بمؤشر الأحدث من تاريخ إعادة التقييم.</span><span class="sxs-lookup"><span data-stu-id="7032c-106">To revalue the lease payments from the **Index rate type** page, the index rate revaluation process uses the most recent index rate from the date of revaluation.</span></span>

<span data-ttu-id="7032c-107">لإضافة أنواع سعر الفائدة المرتبط بمؤشر وسعر الفائدة المرتبط بمؤشر، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="7032c-107">To add index rate types and index rates, follow these steps.</span></span>

1. <span data-ttu-id="7032c-108">انتقل إلى **تأجير الأصول \> الضبط \> أنواع سعر الفائدة المرتبط بمؤشر**.</span><span class="sxs-lookup"><span data-stu-id="7032c-108">Go to **Asset leasing \> Setup \> Index rate type**.</span></span>
2. <span data-ttu-id="7032c-109">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="7032c-109">Select **New**.</span></span>
3. <span data-ttu-id="7032c-110">في الحقول المناسبة، أدخل نوع سعر الفائدة واسم سعر الفائدة المرتبط بمؤشر.</span><span class="sxs-lookup"><span data-stu-id="7032c-110">In the appropriate fields, enter the rate type and the name of the index rate.</span></span>
4. <span data-ttu-id="7032c-111">لإضافة قيمة سعر الفائدة المرتبط بمؤشر جديدة، حدد نوع سعر الفائدة المرتبط بمؤشر، ثم حدد **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="7032c-111">To add a new index rate value, select the index rate type, and then select **Add**.</span></span>
5. <span data-ttu-id="7032c-112">حدد تاريخ البدء الساري لسعر الفائدة، ثم حدد قيمة سعر الصرف.</span><span class="sxs-lookup"><span data-stu-id="7032c-112">Select the effective start date of the rate, and select the rate value.</span></span>

<span data-ttu-id="7032c-113">يجب تحديد إما **فرق قيمة سعر الفائدة المرتبط بمؤشر** أو **قيمة سعر الفائدة المرتبط بمؤشر** كأسلوب سعر الفائدة المرتبط بمؤشر.</span><span class="sxs-lookup"><span data-stu-id="7032c-113">You must select either **Index rate value difference** or **Index rate value** as the index rate method.</span></span>

- <span data-ttu-id="7032c-114">حدد الأسلوب **فرق قيمة سعر الفائدة المرتبط بمؤشر** لحساب دفعات الإيجار جديدة، استنادًا إلى الفرق بين سعر الفائدة المرتبط بمؤشر في تاريخ البدء وأحدث سعر الفائدة المرتبط بمؤشر.</span><span class="sxs-lookup"><span data-stu-id="7032c-114">Select the **Index rate value difference** method to calculate a new lease payment, based on the difference between the index rate on the start date and the most recent index rate.</span></span> <span data-ttu-id="7032c-115">يتم تعريف سعر الفائدة المرتبط بمؤشر في الحقل **سعر الفائدة المرتبط بمؤشر (%)**.</span><span class="sxs-lookup"><span data-stu-id="7032c-115">The index rate is defined in the **Index rate (%)** field.</span></span>
- <span data-ttu-id="7032c-116">حدد أسلوب **قيمة سعر الفائدة المرتبط بمؤشر** لحساب دفعات الإيجار باستخدام النسبة المئوية المحددة في الحقل **سعر الفائدة المرتبط بمؤشر (%)**.</span><span class="sxs-lookup"><span data-stu-id="7032c-116">Select the **Index rate value** method to calculate the lease payment by using the percentage that is specified in the **Index rate (%)** field.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]