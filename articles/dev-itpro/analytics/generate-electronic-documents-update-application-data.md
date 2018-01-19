---
title: "إنشاء المستندات الإلكترونية وتحديث بيانات التطبيق باستخدام أداة إعداد التقارير الإلكترونية"
description: "يمكنك تصميم تنسيقات التقارير الإلكترونية التي يمكن استخدامها في تطبيق Finance and Operations لإنشاء مستندات إلكترونية صادرة. يمكنك أيضًا تصميم تنسيقات التقارير الإلكترونية التي تحلل المستندات الإلكترونية الواردة وتستخدم المحتوى في هذه المستندات لتحديث بيانات التطبيق."
author: NickSelin
manager: AnnBe
ms.date: 11/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: ERSolutionTable, ERVendorTable, ERWorkspace
audience: Developer, IT Pro, Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 27621
ms.assetid: 018a11ae-854c-4f36-9358-8c39baca882d
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ceea24519d641c676521771cee274feb64ca7783
ms.openlocfilehash: 34654c458ce74bf2ee6c2d2bac655d6c399ca393
ms.contentlocale: ar-sa
ms.lasthandoff: 01/19/2018

---

# <a name="generate-electronic-documents-and-update-application-data-using-the-electronic-reporting-tool"></a><span data-ttu-id="ca408-104">إنشاء المستندات الإلكترونية وتحديث بيانات التطبيق باستخدام أداة إعداد التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="ca408-104">Generate electronic documents and update application data using the Electronic reporting tool</span></span>

<span data-ttu-id="ca408-105">يمكنك تصميم تنسيقات التقارير الإلكترونية التي يمكن استخدامها في تطبيق Finance and Operations لإنشاء مستندات إلكترونية صادرة.</span><span class="sxs-lookup"><span data-stu-id="ca408-105">You can design Electronic reporting (ER) formats that can be used in the Finance and Operations application to generate outgoing electronic documents.</span></span> <span data-ttu-id="ca408-106">يمكنك أيضًا تصميم تنسيقات التقارير الإلكترونية التي تحلل المستندات الإلكترونية الواردة وتستخدم المحتوى في هذه المستندات لتحديث بيانات التطبيق.</span><span class="sxs-lookup"><span data-stu-id="ca408-106">You can also design ER formats that parse incoming electronic documents and use the content in those documents to update application data.</span></span> 

<span data-ttu-id="ca408-107">باستخدام هذه الميزة، يمكن استخدام تنسيق تقارير إلكترونية واحد لإنشاء المستندات الإلكترونية الصادرة ثم تحديث بيانات التطبيق.</span><span class="sxs-lookup"><span data-stu-id="ca408-107">With this functionality, a single ER format can be used to generate outgoing electronic documents and then update the application data.</span></span> <span data-ttu-id="ca408-108">يمكن استخدام هذه الميزة في السيناريوهات التالية:</span><span class="sxs-lookup"><span data-stu-id="ca408-108">This feature can be used in the following scenarios:</span></span>

- <span data-ttu-id="ca408-109">لمنع الاستخدام المتكرر لبيانات التطبيق في عمليات لاحقة، يمكنك وضع علامة على بيانات التطبيق مباشرة بعد استخدامها لإنشاء المستندات الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="ca408-109">To prevent repeated usage of application data in subsequent processes you can mark an application’s data immediately after it is used to generate electronic documents.</span></span> <span data-ttu-id="ca408-110">على سبيل المثال، يمكنك وضع علامة على حركات الدفع كحركات تمت معالجتها مباشرةً بعد تضمينها في رسالة الدفع الناشئة.</span><span class="sxs-lookup"><span data-stu-id="ca408-110">For example, you can mark payment transactions as already processed immediately after they have been included in a generated payment message.</span></span>
- <span data-ttu-id="ca408-111">لتخزين تفاصيل معالجة المستندات الإلكترونية التي تم إنشاؤها باستخدام منطق التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="ca408-111">To store the processing details of electronic documents that have been generated using ER logic.</span></span> <span data-ttu-id="ca408-112">على سبيل المثال، تعريف رسالة دفع فريد يتم إنشاؤه باستخدام تعبير التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="ca408-112">For example, a unique payment message identification that is generated using the ER expression.</span></span> <span data-ttu-id="ca408-113">يستند التعبير إلى المعلومات التي تم إدخالها في مربع حوار التقارير الإلكترونية عند تشغيل تنسيق التقارير الإلكترونية لإنشاء المستندات.</span><span class="sxs-lookup"><span data-stu-id="ca408-113">The expression is based on information entered in the ER dialog box when the ER format is run to generate documents.</span></span>

<span data-ttu-id="ca408-114">لمزيد من المعلومات حول هذه الميزة، قم بتشغيل مجموعة دلائل المهام الخاصة بالتقارير الإلكترونية "إنشاء المستندات باستخدام تحديث بيانات التطبيق" (جزء من العملية التجارية اكتساب/تطوير مكونات الخدمات/الحلول الخاصة بتقنية المعلومات)، التي ستنقلك عبر تفاصيل التقارير والأرشفة في نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي.</span><span class="sxs-lookup"><span data-stu-id="ca408-114">To learn more about this feature, play the set of ER Generate documents with application data update Task guides (part of the 7.5.4.3 Acquire/Develop IT service/solution components (10677) business process), which walk you through the details of Intrastat reporting and archiving.</span></span> <span data-ttu-id="ca408-115">الملفات التالية مطلوبة لإكمال بعض الخطوات في دلائل المهام هذه.</span><span class="sxs-lookup"><span data-stu-id="ca408-115">The following files are required to complete certain steps in these Task guides.</span></span> <span data-ttu-id="ca408-116">قم بتنزيل وحفظ هذه الملفات في جهازك المحلي.</span><span class="sxs-lookup"><span data-stu-id="ca408-116">Download and save these files to your local machine.</span></span>

- [<span data-ttu-id="ca408-117">تكوين نموذج بيانات التقارير الإلكترونية: نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي (نموذج)</span><span class="sxs-lookup"><span data-stu-id="ca408-117">ER data model configuration: Intrastat (model)</span></span>](https://go.microsoft.com/fwlink/?linkid=849038)
- [<span data-ttu-id="ca408-118">تكوين تعيين نموذج التقارير الإلكترونية: نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي (التعيين)</span><span class="sxs-lookup"><span data-stu-id="ca408-118">ER model mapping configuration: Intrastat (mapping)</span></span>](https://go.microsoft.com/fwlink/?linkid=849038)
- [<span data-ttu-id="ca408-119">تكوين تنسيق التقارير الإلكترونية: نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي (التنسيق)</span><span class="sxs-lookup"><span data-stu-id="ca408-119">ER format configuration: Intrastat (format)</span></span>](https://go.microsoft.com/fwlink/?linkid=849038)

