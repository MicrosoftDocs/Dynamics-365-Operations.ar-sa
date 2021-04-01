---
title: إعادة تصنيف الجزء قصير الأجل من التزامات الإيجار
description: يوضح هذا الموضوع كيفية إنشاء إدخال دفتر يومية شهريًا لإعادة تصنيف جزء من التزامات الإيجار على أنه قصير أجل.
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
ms.openlocfilehash: 9189033987a3072c7122e1a198768d9de6aa2a52
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5254073"
---
# <a name="reclassify-the-short-term-portion-of-lease-liability"></a><span data-ttu-id="fc67d-103">إعادة تصنيف الجزء قصير الأجل من التزامات الإيجار</span><span class="sxs-lookup"><span data-stu-id="fc67d-103">Reclassify the short-term portion of lease liability</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fc67d-104">يوضح هذا الموضوع كيفية إنشاء إدخال دفتر يومية شهريًا لإعادة تصنيف جزء من التزامات الإيجار على أنه قصير أجل.</span><span class="sxs-lookup"><span data-stu-id="fc67d-104">This topic explains how to create a monthly journal entry to reclassify a portion of the lease liability as short-term.</span></span> <span data-ttu-id="fc67d-105">عندما يكون الجدول الذي يتم تحديده في معالجة الدُفعة عبارة عن **إعادة تصنيف التزامات الإيجار قصيرة الأجل**، فإنه يتم إنشاء إدخال دفتر اليومية.</span><span class="sxs-lookup"><span data-stu-id="fc67d-105">When the schedule that is selected in the batch process is **Short-term lease liability reclass**, a journal entry is created.</span></span> <span data-ttu-id="fc67d-106">يستخدم هذا الإدخال لترحيل الجزء الحالي من التزام الإيجار في اليوم الأخير من الشهر.</span><span class="sxs-lookup"><span data-stu-id="fc67d-106">This entry is used to post the current portion of the lease liability on the last day of the month.</span></span> <span data-ttu-id="fc67d-107">وفي نفس الوقت، يتم ترحيل إدخال الإلغاء اعتبارًا من اليوم الأول من الشهر التالي.</span><span class="sxs-lookup"><span data-stu-id="fc67d-107">At the same time, a reversal entry is posted as of the first day of the next month.</span></span>

<span data-ttu-id="fc67d-108">يتم عرض الجزء الخاص بالفترة القصيرة من التزامات الإيجار في جدول إهلاك الالتزام.</span><span class="sxs-lookup"><span data-stu-id="fc67d-108">The short-term portion of the lease liability is shown on the liability amortization schedule.</span></span> <span data-ttu-id="fc67d-109">عند ترحيل إدخال دفتر اليومية، يصبح العمود **إعادة تصنيف الالتزام لدفتر اليومية الذي تم إنشاءه** متاحًا، ويتم أيضًا ملء معرف دفتر اليومية بالجدول.</span><span class="sxs-lookup"><span data-stu-id="fc67d-109">When the journal entry is posted, the **Liability reclass journal created** column becomes available, and the journal ID is also filled in on the schedule.</span></span>

<span data-ttu-id="fc67d-110">لإنشاء إدخال دفتر اليومية الخاص بإدخال دفتر يومية إعادة التصنيف للالتزام قصير الأجل وترحيله، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="fc67d-110">To create and post the short-term liability reclassification journal entry, follow these steps.</span></span>

1. <span data-ttu-id="fc67d-111">انتقل إلى **تأجير الأصول \> دوري \> إنشاء دفتر يومية الدُفعة**.</span><span class="sxs-lookup"><span data-stu-id="fc67d-111">Go to **Asset leasing \> Periodic \> Batch journal creation**.</span></span>
2. <span data-ttu-id="fc67d-112">في مربع الحوار **إنشاء دفتر يومية الدُفعة**، في الحقل **تحديد جدول**، حدد **إعادة تصنيف التزام الإيجار قصير الأجل**.</span><span class="sxs-lookup"><span data-stu-id="fc67d-112">In the **Batch journal creation** dialog box, in the **Select schedule** field, select **Short-term lease liability reclass**.</span></span>
3. <span data-ttu-id="fc67d-113">في الحقل **مجموعة الإيجار**، حدد مجموعة إيجار.</span><span class="sxs-lookup"><span data-stu-id="fc67d-113">In the **Lease group** field, select a lease group.</span></span> <span data-ttu-id="fc67d-114">أو بدلاً من ذلك، في الحقل **معرف الدفتر**، حدد معرف الدفتر.</span><span class="sxs-lookup"><span data-stu-id="fc67d-114">Alternatively, in the **Book ID** field, select the book ID.</span></span>
4. <span data-ttu-id="fc67d-115">قم بتشغيل المعلمة **ترحيل**.</span><span class="sxs-lookup"><span data-stu-id="fc67d-115">Turn on the **Post** parameter.</span></span> <span data-ttu-id="fc67d-116">وبدلاً من ذلك، إذا كان من الضروري إنشاء الإدخال ولكن لم يتم ترحيله، قم بإيقاف تشغيل هذه المعلمة.</span><span class="sxs-lookup"><span data-stu-id="fc67d-116">Alternatively, if the entry should be created but not posted, leave this parameter turned off.</span></span>
5. <span data-ttu-id="fc67d-117">قم بتشغيل المعلمة **معاينة قبل الترحيل** لعرض الإدخال قبل ترحيله.</span><span class="sxs-lookup"><span data-stu-id="fc67d-117">Turn on the **Preview before posting** parameter to view the entry before it's posted.</span></span>
6. <span data-ttu-id="fc67d-118">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="fc67d-118">Select **OK**.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]