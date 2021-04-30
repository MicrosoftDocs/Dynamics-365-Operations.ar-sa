---
title: قواعد إيجار الأصول
description: يصف هذا الموضوع قواعد الأصول المؤجرة.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLease
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2021-1-28
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 67c4d2b7162cf6bda2eedfecef43ff0b216e6e6c
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/13/2021
ms.locfileid: "5881798"
---
# <a name="asset-leasing-conventions"></a><span data-ttu-id="d5527-103">قواعد إيجار الأصول</span><span class="sxs-lookup"><span data-stu-id="d5527-103">Asset leasing conventions</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="d5527-104">يصف هذا الموضوع قواعد الأصول المؤجرة.</span><span class="sxs-lookup"><span data-stu-id="d5527-104">This topic describes conventions for leased assets.</span></span> <span data-ttu-id="d5527-105">يتم استخدام قواعد الأيجار لتحديد تاريخ البدء لدفتر الإيجار.</span><span class="sxs-lookup"><span data-stu-id="d5527-105">Leasing conventions are used to determine the commencement date of a lease book.</span></span> <span data-ttu-id="d5527-106">في حاله تعيين قاعدة الإيجار على **بلا**، يكون تاريخ البدء هو نفسه تاريخ البدء لعقد الإيجار (أي، قيمة حقل **تاريخ بدء الإيجار**).</span><span class="sxs-lookup"><span data-stu-id="d5527-106">If the leasing convention is set to **None**, the commencement date is the same as the start date for the lease (that is, the value of the **Lease start date** field).</span></span> <span data-ttu-id="d5527-107">في حاله تعيين قاعدة الإيجار على **شهر كامل**، فان التاريخ البدء هو اليوم الأول من الشهر الذي يقع فيه تاريخ بدء الإيجار.</span><span class="sxs-lookup"><span data-stu-id="d5527-107">If the leasing convention is set to **Full month**, the commencement date is the first day of the month that the lease's start date falls in.</span></span>

<span data-ttu-id="d5527-108">يحدد تاريخ البدء تاريخ البدء للفترة الخاصة بإطفاء دين الالتزام وجداول اهلاك الأصول.</span><span class="sxs-lookup"><span data-stu-id="d5527-108">The commencement date determines the start date of the period for the liability amortization and asset depreciation schedules.</span></span> <span data-ttu-id="d5527-109">يتم ترحيل مصروفات الفائدة ومصروفات الإهلاك في تاريخ انتهاء فترة الجداول المقابلة.</span><span class="sxs-lookup"><span data-stu-id="d5527-109">Interest expenses and depreciation expenses are posted on the period end date of the corresponding schedules.</span></span> <span data-ttu-id="d5527-110">يتم ترحيل إدخال دفتر اليومية الخابص بالتقييم الأولي والتسوية في التاريخ البدء.</span><span class="sxs-lookup"><span data-stu-id="d5527-110">The initial recognition and adjustment journal entry are posted on the commencement date.</span></span>

> [!NOTE]
> <span data-ttu-id="d5527-111">يجب تشغيل ميزة قاعدة الإيجار عن طريق إدارة الميزات.</span><span class="sxs-lookup"><span data-stu-id="d5527-111">The feature for leasing conventions must be turned on through Feature Management.</span></span> <span data-ttu-id="d5527-112">في مساحة عمل **إدارة الميزات**، ابحث عن الميزة المسماة **قاعدة الإيجار لتأجير الأصول** وحددها، ثم حدد **التمكين الآن**.</span><span class="sxs-lookup"><span data-stu-id="d5527-112">In the **Feature management** workspace, find and select the feature that is named **Leasing convention for asset leasing** feature, and then select **Enable now**.</span></span>

<span data-ttu-id="d5527-113">يتم تعيين قواعد الإيجار لإعداد دفتر أصول الإيجار.</span><span class="sxs-lookup"><span data-stu-id="d5527-113">Leasing conventions are assigned to the setup for a lease asset book.</span></span>

<span data-ttu-id="d5527-114">لعرض أو تعيين قاعدة الإيجار، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="d5527-114">To view or assign the leasing convention, follow these steps.</span></span>

1. <span data-ttu-id="d5527-115">انتقل إلى **تأجير الأصول \> الضبط \> دفاتر عقد الإيجار**.</span><span class="sxs-lookup"><span data-stu-id="d5527-115">Go to **Asset leasing \> Setup \> Lease books**.</span></span>
2. <span data-ttu-id="d5527-116">في حقل **قاعدة الإيجار**، حدد إحدى القيم التالية.</span><span class="sxs-lookup"><span data-stu-id="d5527-116">In the **Leasing convention** field, select one of the following values.</span></span>

    | <span data-ttu-id="d5527-117">قاعدة التأجير</span><span class="sxs-lookup"><span data-stu-id="d5527-117">Leasing convention</span></span> | <span data-ttu-id="d5527-118">الوصف</span><span class="sxs-lookup"><span data-stu-id="d5527-118">Description</span></span> |
    |--------------------|-------------|
    | <span data-ttu-id="d5527-119">لا شيء</span><span class="sxs-lookup"><span data-stu-id="d5527-119">None</span></span>               | <span data-ttu-id="d5527-120">تبدأ جداول إطفاء دين الالتزام وإهلاك الأصول في تاريخ بدء عقد الإيجار، نظرا لأن تاريخ البدوء يساوي تاريخ بدء الإيجار.</span><span class="sxs-lookup"><span data-stu-id="d5527-120">The liability amortization and asset depreciation schedules start on the lease's start date, because the commencement date equals the lease's start date.</span></span> <span data-ttu-id="d5527-121">وتاريخ الانتهاء هو بعد ذلك بشهر واحد.</span><span class="sxs-lookup"><span data-stu-id="d5527-121">The end date is one month later.</span></span> <span data-ttu-id="d5527-122">ولا تضمن قاعدة الإيجار هذه ترحيل الفائدة في اليوم الأخير من كل شهر.</span><span class="sxs-lookup"><span data-stu-id="d5527-122">This leasing convention doesn't guarantee that the interest will be posted on the last day of each month.</span></span> |
    | <span data-ttu-id="d5527-123">شهر كامل</span><span class="sxs-lookup"><span data-stu-id="d5527-123">Full month</span></span>         | <span data-ttu-id="d5527-124">بالنسبة للإيجارات التي لها تاريخ بدء في أي وقت أثناء الشهر، تبدأ جداول إطفاء دين الالتزام وإهلاك الأصول في استحقاق المصروفات في اليوم الأول من هذا الشهر.</span><span class="sxs-lookup"><span data-stu-id="d5527-124">For leases that have a start date that occurs at any time during the month, the liability amortization and asset depreciation schedules start to accrue expenses on the first day of that month.</span></span> <span data-ttu-id="d5527-125">تضمن قاعدة الإيجار هذه استحقاق الفائدة في اليوم الأخير من كل شهر للشهر بالكامل.</span><span class="sxs-lookup"><span data-stu-id="d5527-125">This leasing convention ensures that interest is accrued on the last day of each month for the whole month.</span></span> |

3. <span data-ttu-id="d5527-126">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="d5527-126">Select **Save**.</span></span>

<span data-ttu-id="d5527-127">عند إنشاء عقد إيجار، يتم إدخال تاريخ البدء لكل دفتر تلقائيًا استنادا إلى تاريخ البدء الذي تم إدخاله للإيجار وقاعدة الإيجار التي يتم تحديدها للدفتر.</span><span class="sxs-lookup"><span data-stu-id="d5527-127">When a lease is created, the commencement date of each book is automatically entered based on the start date that is entered for the lease and the leasing convention that is specified for the book.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
