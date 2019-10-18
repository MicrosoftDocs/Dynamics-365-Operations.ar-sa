---
title: نظرة عامة على قوالب السجلات
description: تقدم هذه المقالة مفهوم قوالب السجلات وتشرح كيفية استخدامها لإنشاء سجلات تشارك المعلومات.
author: pvillads
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 16101
ms.assetid: 61ada2d8-84c3-44bc-b4c5-516b1aeac3d1
ms.search.region: Global
ms.author: pvillads
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5a8f924a5c2dad45d2006240230b85592d56e676
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/27/2019
ms.locfileid: "2176314"
---
# <a name="record-templates-overview"></a><span data-ttu-id="dadf7-103">نظرة عامة على قوالب السجلات</span><span class="sxs-lookup"><span data-stu-id="dadf7-103">Record templates overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="dadf7-104">تقدم هذه المقالة مفهوم قوالب السجلات وتشرح كيفية استخدامها لإنشاء سجلات تشارك المعلومات.</span><span class="sxs-lookup"><span data-stu-id="dadf7-104">This article introduces the concept of record templates and explains how they can be used to create records that share information.</span></span>

<span data-ttu-id="dadf7-105">يُمكن لقوالب التسجيل مساعدتك في إنشاء السجلات بشكل أسرع، ولكن تقتصر هذه الميزة على إنشاء قوالب سجلات لبعض أنواع السجلات.</span><span class="sxs-lookup"><span data-stu-id="dadf7-105">Record templates can help you to create records more quickly, however you can only create record templates for some record types.</span></span>

<span data-ttu-id="dadf7-106">على سبيل المثال، تخيل كنت تقوم بإدخال معلومات إيجار لشركة تأجير سيارات موجودة في سان فرانسيسكو.</span><span class="sxs-lookup"><span data-stu-id="dadf7-106">For example, imagine you are entering rental information for a car rental business that is located in San Francisco.</span></span> <span data-ttu-id="dadf7-107">ولأن معظم العملاء ربما من منطقة سان فرانسيسكو، سيكون جميلا إذا تمكنت من ملء القيم تلقائياً في حقول **الحالة**، و**البلد**، و**المدينة** في نموذج التأجير.</span><span class="sxs-lookup"><span data-stu-id="dadf7-107">Since most of the customers are likely to be from the San Francisco area, it would be nice if you could automatically fill in the values for the **State**, **Country**, and **City** fields on the rental form.</span></span>

> [!NOTE]
> <span data-ttu-id="dadf7-108">يمكنك تطبيق القوالب على المناطق التي يكون لك حق الوصول إليها فقط.</span><span class="sxs-lookup"><span data-stu-id="dadf7-108">You can apply templates only in areas that you have access to.</span></span> <span data-ttu-id="dadf7-109">ومع ذلك، يمكنك رؤية كافة عناوين القوالب عند إنشاء سجل جديد، ويمكن للمستخدمين الآخرين رؤيتها أيضًا، وذلك في حالة إنشاء القوالب التي ستكون متوفرة لكافة المستخدمين.</span><span class="sxs-lookup"><span data-stu-id="dadf7-109">However all template titles are visible to you when you create a new record, and to other users as well, if you are creating templates that will be available for all users.</span></span> <span data-ttu-id="dadf7-110">تأكد من ذلك عند القيام بتسمية القوالب.</span><span class="sxs-lookup"><span data-stu-id="dadf7-110">Be sure to consider this when naming templates.</span></span> <span data-ttu-id="dadf7-111">فعلى سبيل المثال، تجنب استخدام أسماء تحتوي على كلمات مثل "العمولة"، إذا كان يُعد حصول بعض الموظفين في الشركة على رواتب تعتمد على العمولات أمرًا سريًا.</span><span class="sxs-lookup"><span data-stu-id="dadf7-111">For example, avoid using names that include words, such as "commission," if is confidential that some employees in the company have commission-based salaries.</span></span>

<span data-ttu-id="dadf7-112">إذا كان يوجد قالب واحد أو أكثر يكون لك حق الوصول إليه في نموذج معين وأنت تحاول إنشاء سجل جديد في النموذج، يتم عرض النموذج **تحديد قالب لـ**.</span><span class="sxs-lookup"><span data-stu-id="dadf7-112">When one or more templates that you have access to exist for a specific form and you attempt to create a new record in the form, the **Select a template for** page is displayed.</span></span> <span data-ttu-id="dadf7-113">وعند تحديد قالب من القائمة، يتم إنشاء السجل الجديد والذي يحتوي على معلومات افتراضية مستندة إلى القالب الذي حددته.</span><span class="sxs-lookup"><span data-stu-id="dadf7-113">When you select a template from the list, the new record is created and contains default information that is based on the template that you selected.</span></span> <span data-ttu-id="dadf7-114">إذا كنت لا تريد استخدام القوالب عند إنشاء سجلات جديدة، فحدد خانة الاختيار **عدم السؤال مرة أخرى** في الصفحة **‏‫تحديد قالب لـ**.</span><span class="sxs-lookup"><span data-stu-id="dadf7-114">If you do not want to use templates when you create new records, select the **Do not ask again** check box in the **Select a template for** page.</span></span> <span data-ttu-id="dadf7-115">لعرض مربع حوار تحديد القالب مرة أخرى، انقر بزر الماوس الأيمن فوق أي سجل، ثم انقر فوق **‏‫معلومات السجل**، ثم **‏‫إظهار تحديد القالب‬**.</span><span class="sxs-lookup"><span data-stu-id="dadf7-115">To display the template selection dialog box again, right-click any record, click **Record info**, and then click **Show template selection**.</span></span>
