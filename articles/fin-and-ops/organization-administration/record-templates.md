---
title: "قوالب السجل"
description: "تقدم هذه المقالة مفهوم قوالب السجلات وتشرح كيفية استخدامها لإنشاء سجلات تشارك المعلومات."
author: pvillads
manager: AnnBe
ms.date: 08/18/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 16101
ms.assetid: 61ada2d8-84c3-44bc-b4c5-516b1aeac3d1
ms.search.region: Global
ms.author: pvillads
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: e89e4a74550597a4e497a1128fe91c07e766d697
ms.contentlocale: ar-sa
ms.lasthandoff: 09/29/2017

---

# <a name="record-templates"></a><span data-ttu-id="f231d-103">قوالب السجل</span><span class="sxs-lookup"><span data-stu-id="f231d-103">Record templates</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="f231d-104">تقدم هذه المقالة مفهوم قوالب السجلات وتشرح كيفية استخدامها لإنشاء سجلات تشارك المعلومات.</span><span class="sxs-lookup"><span data-stu-id="f231d-104">This article introduces the concept of record templates and explains how they can be used to create records that share information.</span></span>

<span data-ttu-id="f231d-105">يمكن أن تساعدك قوالب السجل على إنشاء سجلات بشكل أسرع في Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="f231d-105">Record templates can help you to create records more quickly in Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="f231d-106">ويمكن أن تنشئ قوالب السجل لبعض أنوع السجلات فقط في Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="f231d-106">You can create record templates for only some of the record types in Microsoft Dynamics 365 for Finance and Operations.</span></span> 

<span data-ttu-id="f231d-107">على سبيل المثال، تخيل كنت تقوم بإدخال معلومات إيجار لشركة تأجير سيارات موجودة في سان فرانسيسكو.</span><span class="sxs-lookup"><span data-stu-id="f231d-107">For example, imagine you are entering rental information for a car rental business that is located in San Francisco.</span></span> <span data-ttu-id="f231d-108">ولأن معظم العملاء ربما من منطقة سان فرانسيسكو، سيكون جميلا إذا تمكنت من ملء القيم تلقائياً في حقول **الحالة**، و**البلد**، و**المدينة** في نموذج التأجير.</span><span class="sxs-lookup"><span data-stu-id="f231d-108">Since most of the customers are likely to be from the San Francisco area, it would be nice if you could automatically fill in the values for the **State**, **Country**, and **City** fields on the rental form.</span></span> 

> [!Note]
> <span data-ttu-id="f231d-109">يمكنك تطبيق القوالب فقط على مناطق Finance and Operations التي لديك حق الوصول إليها.</span><span class="sxs-lookup"><span data-stu-id="f231d-109">You can apply templates only for the areas of Finance and Operations that you have access to.</span></span> <span data-ttu-id="f231d-110">ومع ذلك، يمكنك رؤية كافة عناوين القوالب عند إنشاء سجل جديد، ويمكن للمستخدمين الآخرين رؤيتها أيضًا، وذلك في حالة إنشاء القوالب التي ستكون متوفرة لكافة المستخدمين.</span><span class="sxs-lookup"><span data-stu-id="f231d-110">However all template titles are visible to you when you create a new record, and to other users as well, if you are creating templates that will be available for all users.</span></span> <span data-ttu-id="f231d-111">تأكد من ذلك عند القيام بتسمية القوالب.</span><span class="sxs-lookup"><span data-stu-id="f231d-111">Be sure to consider this when naming templates.</span></span> <span data-ttu-id="f231d-112">فعلى سبيل المثال، تجنب استخدام أسماء تحتوي على كلمات مثل "العمولة"، إذا كان يُعد حصول بعض الموظفين في الشركة على رواتب تعتمد على العمولات أمرًا سريًا.</span><span class="sxs-lookup"><span data-stu-id="f231d-112">For example, avoid using names that include words, such as "commission," if is confidential that some employees in the company have commission-based salaries.</span></span> 

<span data-ttu-id="f231d-113">إذا كان يوجد قالب واحد أو أكثر يكون لك حق الوصول إليه في نموذج معين وأنت تحاول إنشاء سجل جديد في النموذج، يتم عرض النموذج **تحديد قالب لـ**.</span><span class="sxs-lookup"><span data-stu-id="f231d-113">When one or more templates that you have access to exist for a specific form and you attempt to create a new record in the form, the **Select a template for** page is displayed.</span></span> <span data-ttu-id="f231d-114">وعند تحديد قالب من القائمة، يتم إنشاء السجل الجديد والذي يحتوي على معلومات افتراضية مستندة إلى القالب الذي حددته.</span><span class="sxs-lookup"><span data-stu-id="f231d-114">When you select a template from the list, the new record is created and contains default information that is based on the template that you selected.</span></span> <span data-ttu-id="f231d-115">إذا كنت لا تريد استخدام القوالب عند إنشاء سجلات جديدة، فحدد خانة الاختيار **عدم السؤال مرة أخرى** في الصفحة **‏‫تحديد قالب لـ**.</span><span class="sxs-lookup"><span data-stu-id="f231d-115">If you do not want to use templates when you create new records, select the **Do not ask again** check box in the **Select a template for** page.</span></span> <span data-ttu-id="f231d-116">لعرض مربع حوار تحديد القالب مرة أخرى، انقر بزر الماوس الأيمن فوق أي سجل، ثم انقر فوق **‏‫معلومات السجل**، ثم **‏‫إظهار تحديد القالب‬**.</span><span class="sxs-lookup"><span data-stu-id="f231d-116">To display the template selection dialog box again, right-click any record, click **Record info**, and then click **Show template selection**.</span></span>



