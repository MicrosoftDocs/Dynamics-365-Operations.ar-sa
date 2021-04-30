---
title: إنشاء إدخالات دفتر اليومية الشهري في مجموعة
description: يوضح هذا الموضوع كيفية إنشاء إدخالات دفتر اليومية في دُفعة للمساعدة في زيادة الكفاءة عند تسجيل مصروفات عقد الإيجار الشهرية.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: Dialog
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: ca84e56569ea5ddbb4d5335d0944a6bd8a50a1b1
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/13/2021
ms.locfileid: "5881194"
---
# <a name="create-monthly-journal-entries-in-a-batch"></a><span data-ttu-id="301ac-103">إنشاء إدخالات دفتر اليومية الشهري في مجموعة</span><span class="sxs-lookup"><span data-stu-id="301ac-103">Create monthly journal entries in a batch</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="301ac-104">يوضح هذا الموضوع كيفية إنشاء إدخالات دفتر اليومية في دُفعة للمساعدة في زيادة الكفاءة عند تسجيل مصروفات عقد الإيجار الشهرية.</span><span class="sxs-lookup"><span data-stu-id="301ac-104">This topic explains how to create journal entries in a batch to help increase efficiency when monthly lease expenses are recorded.</span></span> <span data-ttu-id="301ac-105">يمكن استخدام معالجة الدُفعة لإنشاء إدخالات دفتر اليومية من جداول متعددة.</span><span class="sxs-lookup"><span data-stu-id="301ac-105">Batch processing can be used to create journal entries from multiple schedules.</span></span> <span data-ttu-id="301ac-106">يمكن أن تتضمن إدخالات دفتر اليومية هذه التزامات الإيجار وإطفاء دين الالتزامات وإطفاء دين الأصل بحق استخدام الأصل (ROU) وكذلك مصروفات تكلفة تنفيذ العقد.</span><span class="sxs-lookup"><span data-stu-id="301ac-106">These journal entries can include lease payments, liability amortization, right-of-use (ROU) asset amortization, and executory cost expenses.</span></span> <span data-ttu-id="301ac-107">يمكنك أيضًا استخدام معالجة الدُفعة لإجراء التقييم الأولي على عقود الإيجار المتعددة في نفس الوقت، أو لإنشاء تعديلات انتقالية للعديد من عقود الإيجار في نفس الوقت.</span><span class="sxs-lookup"><span data-stu-id="301ac-107">You can also use batch processing to do the initial recognition of multiple leases at the same time, or to create transition adjustments for multiple leases at the same time.</span></span>

<span data-ttu-id="301ac-108">لإعداد وظيفة دُفعة، أو لمعالجة فواتير الدفع أو الإهلاك أو الفائدة للعديد من عقود الإيجار، انتقل إلى **تأجير الأصول \> دوري \> إنشاء دفتر يومية الدُفعة**.</span><span class="sxs-lookup"><span data-stu-id="301ac-108">To set up a batch job, or to process payment invoices, depreciation, or interest for multiple leases, go to **Asset leasing \> Periodic \> Batch journal creation**.</span></span> <span data-ttu-id="301ac-109">في مربع الحوار الذي يظهر، يمكنك تحديد الجدول الذي يجب إنشاء إدخالات دفتر اليومية منه.</span><span class="sxs-lookup"><span data-stu-id="301ac-109">In the dialog box that appears, you can select the schedule that the journal entries should be created from.</span></span> <span data-ttu-id="301ac-110">يمكنك أيضًا تحديد ما إذا كان ينبغي تشغيل معالجة المجموعة لكيانات معينة أو مجموعات عقود الإيجار أو دفاتر عقود الإيجار.</span><span class="sxs-lookup"><span data-stu-id="301ac-110">You can also specify whether the batch process should be run for specific entities, lease groups, or lease books.</span></span>

> [!NOTE]
> <span data-ttu-id="301ac-111">سيتم ترحيل الحركات اللاحقة، مثل جداول إطفاء دين الالتزامات والدفعات والإهلاك والمصروفات فقط بعد ترحيل الإقرار التقييم الأولي لعقود الإيجار المقابلة.</span><span class="sxs-lookup"><span data-stu-id="301ac-111">Subsequent transactions, such as liability amortization schedules, payments, depreciation, and expenses, will be posted only after the initial recognition for corresponding leases is posted.</span></span>
>
> <span data-ttu-id="301ac-112">يتم إنشاء إدخالات دفتر اليومية، ولكن لن يتم ترحيلها حتى تقوم بتحديد الأمر **تشغيل**.</span><span class="sxs-lookup"><span data-stu-id="301ac-112">The journal entries are created, but they won't be posted until you select the **Run** command.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
