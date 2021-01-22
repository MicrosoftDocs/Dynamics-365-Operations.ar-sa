---
title: نظرة عامة على الدفع الإيجابي
description: توفر هذه المقالة معلومات حول الدفع الإيجابي الذي يُستخدم لإنشاء قائمة إلكترونية بالشيكات التي يمكن تقديمها إلى البنك.
author: panolte
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankPositivePaySummary
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 88463
ms.assetid: 1e3a39d3-f9b3-4073-9730-c96a607243e2
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: f64b2bc6c336ba833cbd95f83596fe516bce8b56
ms.sourcegitcommit: 1b00e21faf89de8b3450936253a4c02cb4d12a3d
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/28/2020
ms.locfileid: "3295213"
---
# <a name="positive-pay-overview"></a><span data-ttu-id="94e99-103">نظرة عامة على الدفع الإيجابي</span><span class="sxs-lookup"><span data-stu-id="94e99-103">Positive pay overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="94e99-104">توفر هذه المقالة معلومات حول الدفع الإيجابي الذي يُستخدم لإنشاء قائمة إلكترونية بالشيكات التي يمكن تقديمها إلى البنك.</span><span class="sxs-lookup"><span data-stu-id="94e99-104">This article provides information about positive pay, which is used to generate an electronic list of checks that can be presented to a bank.</span></span> 

<span data-ttu-id="94e99-105">يُستخدم الدفع الإيجابي لإنشاء قائمة إلكترونية بالشيكات التي يمكن تقديمها إلى البنك.</span><span class="sxs-lookup"><span data-stu-id="94e99-105">Positive pay is used to generate an electronic list of checks that can be presented to a bank.</span></span> <span data-ttu-id="94e99-106">بإمكان ملفات الدفع الإيجابي أن تساعد البنوك على منع تزوير الشيكات المصرفية.</span><span class="sxs-lookup"><span data-stu-id="94e99-106">Positive pay files can help banks prevent check fraud.</span></span> <span data-ttu-id="94e99-107">ستقوم بإعداد الدفع الإيجابي لإنشاء قائمة إلكترونية بالشيكات في كل مرة تتم فيها طباعة الشيكات.</span><span class="sxs-lookup"><span data-stu-id="94e99-107">You set up positive pay to generate an electronic list of checks every time that checks are printed.</span></span> <span data-ttu-id="94e99-108">بعد ذلك، عندما يتم تقديم أحد الشيكات إلى البنك، يقارن البنك الشيك بقائمة الشيكات التي قدمتها في وقت سابق.</span><span class="sxs-lookup"><span data-stu-id="94e99-108">Then, when a check is presented to the bank, the bank compares the check with the list of checks that you previously submitted.</span></span> <span data-ttu-id="94e99-109">إذا تطابق الشيك مع شيك آخر في القائمة، فسيقوم البنك بمخالصته.</span><span class="sxs-lookup"><span data-stu-id="94e99-109">If the check matches a check in the list, the bank clears it.</span></span> <span data-ttu-id="94e99-110">أما إذا لم يتطابق الشيك لم تطابق مع أي شيك آخر في القائمة، فسيحتفظ البنك به لمراجعته.</span><span class="sxs-lookup"><span data-stu-id="94e99-110">If the check doesn't match a check in the list, the bank holds it for review.</span></span>

<span data-ttu-id="94e99-111">يُعرف أيضًا الدفع الإيجابي بالدفع الآمن.</span><span class="sxs-lookup"><span data-stu-id="94e99-111">Positive pay is also known as SafePay.</span></span> 

<span data-ttu-id="94e99-112">يمكن أن تحتوي ملفات الدفع الإيجابي على معلومات هامة حول المستفيدين ومبالغ الشيكات.</span><span class="sxs-lookup"><span data-stu-id="94e99-112">Positive pay files can contain sensitive information about payees and check amounts.</span></span> <span data-ttu-id="94e99-113">لذلك، تأكد من استخدام تدابير أمنية مناسبة اعتبارًا من وقت إنشاء الملفات وحى استلام البنك لها.</span><span class="sxs-lookup"><span data-stu-id="94e99-113">Therefore, make sure that you use appropriate security measures from the time that the files are generated until they are received by the bank.</span></span> <span data-ttu-id="94e99-114">يتم تنزيل ملفات الدفع الإيجابي وفقًا لإرشادات التنزيل لمستعرض ويب.</span><span class="sxs-lookup"><span data-stu-id="94e99-114">Positive pay files are downloaded according to the download instructions for the web browser.</span></span> 

<span data-ttu-id="94e99-115">يتم إنشاء ملفات الدفع الإيجابي باستخدام كيانات البيانات.</span><span class="sxs-lookup"><span data-stu-id="94e99-115">Positive pay files are created by using data entities.</span></span> <span data-ttu-id="94e99-116">وقبل إنشاء ملف دفع إيجابي، يجب إعداد تنسيقات التحويل الخاصة بتنسيق XML الذي يترجم البيانات إلى تنسيق يستطيع البنك استخدامه.</span><span class="sxs-lookup"><span data-stu-id="94e99-116">Before you generate a positive pay file, you must set up the transformation formats for the XML that translates the data into a format that the bank can consume.</span></span> 

<span data-ttu-id="94e99-117">لكل حساب بنكي تريد إنشاء معلومات دفع إيجابي له، يجب تعيين تنسيق الدفع الإيجابي.</span><span class="sxs-lookup"><span data-stu-id="94e99-117">For each bank account that you want to generate positive pay information for, you must assign the positive pay format.</span></span> <span data-ttu-id="94e99-118">بعد إنشاء الدفعات، يمكنك إنشاء ملف دفع إيجابي لكيان قانوني واحد وحساب بنكي واحد.</span><span class="sxs-lookup"><span data-stu-id="94e99-118">After you generate payments, you can generate a positive pay file for a single legal entity and a single bank account.</span></span> <span data-ttu-id="94e99-119">أو، يمكنك إنشاء ملفات الدفع الإيجابي لعدة كيانات قانونية وحسابات بنكية في الوقت نفسه.</span><span class="sxs-lookup"><span data-stu-id="94e99-119">Alternatively, you can generate positive pay files for multiple legal entities and bank accounts at the same time.</span></span> 

<span data-ttu-id="94e99-120">بعد اتمام دفع كل الشيكات المدرجة في ملف الدفع الإيجابي، ستتلقى رقم تأكيد من البنك.</span><span class="sxs-lookup"><span data-stu-id="94e99-120">After the checks that are listed in a positive pay file have been paid, you receive a confirmation number from your bank.</span></span> <span data-ttu-id="94e99-121">يمكنك عندئذٍ تأكيد ملف الدفع الإيجابي في النظام.</span><span class="sxs-lookup"><span data-stu-id="94e99-121">You can then confirm the positive pay file in the system.</span></span> 

<span data-ttu-id="94e99-122">إذا لزم تغيير ملف دفع إيجابي، فيمكنك إعادة استدعائه.</span><span class="sxs-lookup"><span data-stu-id="94e99-122">If you must change a positive pay file, you can recall it.</span></span> <span data-ttu-id="94e99-123">بعد ذلك، ولكل شيك في ملف الدفع الإيجابي، يُعاد تعيين الحقل الذي يشير إلى ما إذا تم تضمين الشيك في ملف دفع إيجابي.</span><span class="sxs-lookup"><span data-stu-id="94e99-123">Then, for each check in the positive pay file, the field that indicates whether that check has been included in a positive pay file is reset.</span></span>

<span data-ttu-id="94e99-124">لمزيد من المعلومات، راجع [إعداد ملفات الدفع الإيجابي وإنشاؤها‬‏‫](set-up-generate-positive-pay-files.md).</span><span class="sxs-lookup"><span data-stu-id="94e99-124">For more information, see [Set up and generate positive pay files](set-up-generate-positive-pay-files.md).</span></span>


