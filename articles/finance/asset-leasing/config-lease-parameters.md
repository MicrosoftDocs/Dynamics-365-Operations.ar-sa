---
title: تكوين محددات عقد الإيجار (معاينة)
description: يصف هذا الموضوع إعدادات التكوين الخاصة بتأجير الأصول، مثل معلومات الأمان وإعدادات المحاسبة.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: ff0aa5fd0b78814dfa5bb00d6d5ef2984c566d14
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "4971393"
---
# <a name="configure-lease-parameters"></a><span data-ttu-id="313e2-103">تكوين محددات عقد الإيجار</span><span class="sxs-lookup"><span data-stu-id="313e2-103">Configure lease parameters</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="313e2-104">وتؤثر إعدادات التكوين المتعددة على سلوك تأجير الأصول.</span><span class="sxs-lookup"><span data-stu-id="313e2-104">Several configuration settings affect how Asset leasing behaves.</span></span> <span data-ttu-id="313e2-105">وتتضمن هذه الإعدادات أسماء دفاتر اليومية والمعلمات العامة وإعدادات ملف تعريف الترحيل.</span><span class="sxs-lookup"><span data-stu-id="313e2-105">These settings include journal names, general parameters, and posting profile settings.</span></span>

1. <span data-ttu-id="313e2-106">انتقل إلى **تأجير الأصول‬ \> الإعداد‬ \> معلمات تأجير الأصول**.</span><span class="sxs-lookup"><span data-stu-id="313e2-106">Go to **Asset leasing \> Setup \> Asset leasing parameters**.</span></span>
2. <span data-ttu-id="313e2-107">في علامة التبويب **عقود الإيجار**، حدد علامة التبويب السريعة **عام**.</span><span class="sxs-lookup"><span data-stu-id="313e2-107">On the **Leases** tab, select the **General** FastTab.</span></span>

    <span data-ttu-id="313e2-108">تحدد المعلمة **السماح بتجاوز التصنيف اليدوي** ما إذا كان من الممكن تجاوز تصنيف عقد الإيجار قبل تأكيد جدول الدفع أم لا.</span><span class="sxs-lookup"><span data-stu-id="313e2-108">The **Allow manual classification override** parameter determines whether the lease classification can be overridden before the payment schedule is confirmed.</span></span>

    <span data-ttu-id="313e2-109">تحدد المعلمة **الدفعة عبر الكيان** ما إذا كان يمكنك الترحيل إلى كيانات قانونية أخرى من الكيان القانوني الحالي أم لا.</span><span class="sxs-lookup"><span data-stu-id="313e2-109">The **Cross-entity batch** parameter determines whether you can post to other legal entities from the current legal entity.</span></span> <span data-ttu-id="313e2-110">في حالة تشغيل هذه المعلمة، فإنه يمكنك إنشاء إدخالات دفتر اليومية للكيانات القانونية التي يمكنك الوصول إليها.</span><span class="sxs-lookup"><span data-stu-id="313e2-110">If this parameter is turned on, you can create journal entries for the legal entities that you have access to.</span></span>

3. <span data-ttu-id="313e2-111">قم بتعيين الخيار **السماح بحذف عقود الإيجار المؤكدة** على **نعم** للسماح بحذف عقود الإيجار التي أكدت على جداول الدفع.</span><span class="sxs-lookup"><span data-stu-id="313e2-111">Set the **Allow delete of confirmed leases** option to **Yes** to allow leases that have confirmed payment schedules to be deleted.</span></span> <span data-ttu-id="313e2-112">لا يمكن حذف عقود الإيجار إذا كانت الحركات المرحلة أو الحركات غير المرحلة مقترنة بها، بغض النظر عن إعداد هذا الخيار.</span><span class="sxs-lookup"><span data-stu-id="313e2-112">Leases can't be deleted if posted or unposted transactions are associated with them, regardless of the setting of this option.</span></span> <span data-ttu-id="313e2-113">لا يمكنك استعادة سجل عقد الإيجار بعد حذفه.</span><span class="sxs-lookup"><span data-stu-id="313e2-113">You can't restore a lease record after it's deleted.</span></span> <span data-ttu-id="313e2-114">إذا قمت بتحميل أية سجلات لعقد إيجار محذوف، فإما يدويًا أو من خلال كيانات البيانات، فإنه يتم التعامل مع المعلومات التي تم تحميلها على أنها جديدة، وليست تحديثًا لعقد إيجار موجود.</span><span class="sxs-lookup"><span data-stu-id="313e2-114">If you upload any records for a deleted lease, either manually or through data entities, the uploaded information is treated as new, not as an update to an existing lease.</span></span>

    <span data-ttu-id="313e2-115">إذا قمت بتعيين هذا الخيار إلى **نعم**، وكان نوع الانتقال الخاص بالدفتر هو **الخيار التسوية التراكمي أ أو ب**، يقوم النظام بتعيين الحقل **سعر الفائدة على الافتراض الإضافي** إلى قيمة الحقل **سعر الفائدة على الافتراض الإضافي عند الانتقال** في الصفحة **إعداد الدفاتر**.</span><span class="sxs-lookup"><span data-stu-id="313e2-115">If you set this option to **Yes**, and the transition type of the book is **Cumulative Catchup Option A or B**, the system sets the **Incremental borrowing rate** field to the value of the **Incremental borrowing rate at transition** field on the **Book setup** page.</span></span> <span data-ttu-id="313e2-116">إذا تم تعيين هذا الخيار إلى **لا**، فإنه يتم تعيين سعر الفائدة الموجود في رأس عقد الإيجار على القيمة **سعر الفائدة على الاقتراض الإضافي** في الصفحة **تفاصيل الدفتر**، بغض النظر عن نوع الانتقال بالدفتر.</span><span class="sxs-lookup"><span data-stu-id="313e2-116">If this option is set to **No**, the rate on the head lease is set to the value of the **Incremental borrowing rate** field on the **Book details** page, regardless of the transition type of the book.</span></span>

4. <span data-ttu-id="313e2-117">قم بتعيين الخيار **السماح بعمليات إلغاء الإهلاك على إصدار الدفتر المغلق** إلى **نعم** للسماح بعكس حركات مصروفات الإهلاك.</span><span class="sxs-lookup"><span data-stu-id="313e2-117">Set the **Allow depreciation reversals on closed book version** option to **Yes** to allow depreciation expense transactions to be reversed.</span></span> <span data-ttu-id="313e2-118">يمكن عكس حركات المصروفات حتى في حالة إغلاق إصدار الدفتر.</span><span class="sxs-lookup"><span data-stu-id="313e2-118">Expense transactions can be reversed even when the book version is closed.</span></span>

    > [!NOTE]
    > <span data-ttu-id="313e2-119">ونوصي بأن تجعل بهذا الخيار معينًا على **لا**.</span><span class="sxs-lookup"><span data-stu-id="313e2-119">We recommend that you keep this option set to **No**.</span></span> <span data-ttu-id="313e2-120">يتم استخدام إعداد هذا الخيار كخيار تحقق من الصحة والتحكم لمنع إهلاك إصدار دفتر مغلق عن طريق الخطأ.</span><span class="sxs-lookup"><span data-stu-id="313e2-120">The setting of this option is used as a validation and control to prevent a closed book version from being accidently depreciated.</span></span> <span data-ttu-id="313e2-121">وبإبقاء الخيار معينًا على **لا**، فإنك تساعد في الاحتفاظ بدقة صافي القيمة الدفترية وحسابات الإهلاك المستقبلية.</span><span class="sxs-lookup"><span data-stu-id="313e2-121">By keeping the option set to **No**, you help keep the net book value and future depreciation calculations accurate.</span></span>
