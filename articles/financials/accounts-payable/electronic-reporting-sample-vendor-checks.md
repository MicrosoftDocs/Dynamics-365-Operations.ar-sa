---
title: "عينة شيكات المورد الخاصة بإعداد التقارير الإلكترونية"
description: "يوفر هذا الموضوع معلومات عامة حول كيفية استخدام عينات تنسيقات الشيكات الخاصة بإعداد التقارير الإلكترونية."
author: twheeloc
manager: AnnBe
ms.date: 06/14/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.assetid: 
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: c583c3d82ce7273c49144561c51cfbec932d3ae8
ms.contentlocale: ar-sa
ms.lasthandoff: 05/08/2018

---

[!include [banner](../includes/banner.md)]

# <a name="electronic-reporting-sample-check-formats"></a><span data-ttu-id="e9928-103">عينات تنسيقات الشيكات الخاصة بإعداد التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="e9928-103">Electronic reporting sample check formats</span></span>

<span data-ttu-id="e9928-104">يمكنك استخدام التقارير الإلكترونية (ER) لتنسيق شيكات المورد.</span><span class="sxs-lookup"><span data-stu-id="e9928-104">You can use Electronic reporting (ER) to format vendor checks.</span></span> <span data-ttu-id="e9928-105">تتوافر ‏‫العديد من تنسيقات الشيكات الخاصة بالبنوك والخاصة بموفري الخدمات في السوق></span><span class="sxs-lookup"><span data-stu-id="e9928-105">Many bank-specific and check provider–specific check formats are available on the market.</span></span> <span data-ttu-id="e9928-106">تم تضمين أمثلة لتنسيقات شيكات في نموذج شيك الدفع في مستودع أداة إعداد التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="e9928-106">Sample check formats have been included in the Payment check model in the ER tool repository.</span></span> <span data-ttu-id="e9928-107">تسمى عينات الشيكات هذه بـ **الشيك في الوسط (الولايات المتحدة)** و **الشيك في أعلى والكعب أسفل (الولايات المتحدة)**.</span><span class="sxs-lookup"><span data-stu-id="e9928-107">These sample checks are labeled **Check in the middle (US)** and **Check on top stub below (US)**.</span></span>

## <a name="what-check-formats-are-currently-supported"></a><span data-ttu-id="e9928-108">ما هي تنسيقات الشيكات المدعومة حاليًا؟</span><span class="sxs-lookup"><span data-stu-id="e9928-108">What check formats are currently supported?</span></span>

<span data-ttu-id="e9928-109">يجب عليك دائمًا الانتقال إلى مكتبة الأصول المشتركة في Microsoft Dynamics Lifecycle Services (LCS) وعرض قائمة بأحدث الملفات المتوفرة التي تحتوي على نوع أصل **تكوين GER**.</span><span class="sxs-lookup"><span data-stu-id="e9928-109">You should always go to the Shared asset library in Microsoft Dynamics Lifecycle Services (LCS) and view the current list of available files that have an asset type of **GER configuration**.</span></span> <span data-ttu-id="e9928-110">يتضمن القسم التالي، "ما الذي يجب عليّ إعداده؟، ارتباطًا إلى الموضوع الذي يشرح كيفية إنشاء مستودع LCS، بحيث تتمكن من مراجعة التكوينات المتوفرة واستيراد تكوينات محددة.</span><span class="sxs-lookup"><span data-stu-id="e9928-110">The next section, “What do I have to set up?,” includes a link to a topic that explains how to create an LCS repository so that you can review available configurations and import selected configurations.</span></span>

<span data-ttu-id="e9928-111">يتضمن Microsoft Dynamics 365 for Finance and Operations عينة تنسيق يوجد فيه الشيك في الأعلى، ويليه قسمين للحوالات.</span><span class="sxs-lookup"><span data-stu-id="e9928-111">Microsoft Dynamics 365 for Finance and Operations, includes a sample format where the check is on top, followed by two remittance sections.</span></span> <span data-ttu-id="e9928-112">ويتضمن أيضًا عينة تنسيق يكون فيها الشيك في الوسط بين قسمي الحوالة.</span><span class="sxs-lookup"><span data-stu-id="e9928-112">It also includes a sample format where the check is in the middle, between two remittance sections.</span></span> <span data-ttu-id="e9928-113">تتوافق عينات التنسيقات هذه مع تنسيقات شيكات أعمال Deluxe.</span><span class="sxs-lookup"><span data-stu-id="e9928-113">These sample formats correspond to Deluxe business checks formats.</span></span>

## <a name="what-do-i-have-to-set-up"></a><span data-ttu-id="e9928-114">ما الذي يجب عليَّ إعداده؟</span><span class="sxs-lookup"><span data-stu-id="e9928-114">What do I have to set up?</span></span>

- <span data-ttu-id="e9928-115">قبل أن تتمكن من طباعة الشيكات باستخدام التقارير الإلكترونية، فمن ثم يجب استيراد تكوين شيك نشط واحد على الأقل إلى تكوينات التقارير الإلكترونية الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="e9928-115">Before you can print checks by using ER, at least one active check configuration must be imported into your ER configurations.</span></span> <span data-ttu-id="e9928-116">للمزيد من التعليمات، راجع [تنزيل تكوينات التقارير الإلكترونية من Lifecycle Services](../../dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md)</span><span class="sxs-lookup"><span data-stu-id="e9928-116">For instructions, see [Download Electronic reporting configurations from Lifecycle Services](../../dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).</span></span>
- <span data-ttu-id="e9928-117">عندما تقوم بتكوين الشيكات النقدية وشيكات الإدارة البنكية للحساب البنكي، حدد خانة اختيار **تنسيق تصدير إلكتروني عام**، ثم حدد تنسيق الشيك المناسب كتكوين تنسيق ملف تصدير.</span><span class="sxs-lookup"><span data-stu-id="e9928-117">When you configure Cash and bank management checks for the bank account, select the **Generic electronic Export format** check box, and then select the appropriate check format as an export format configuration.</span></span>
- <span data-ttu-id="e9928-118">يجب عليك أيضا تحديد عدد أسطر الإيصال التي سوف تتم طباعتها على الحوالة.</span><span class="sxs-lookup"><span data-stu-id="e9928-118">You must also specify the number of slip lines that will be printed on the remittance.</span></span> <span data-ttu-id="e9928-119">تأكد من تضمين صفوف الرؤوس عند حساب هذا الرقم.</span><span class="sxs-lookup"><span data-stu-id="e9928-119">Be sure to include the header rows when you calculate this number.</span></span> <span data-ttu-id="e9928-120">بالنسبة لعينتي تنسيق الشيك، يبلغ عدد أسطر الإيصال الموصي بها هي 17 سطرًا.</span><span class="sxs-lookup"><span data-stu-id="e9928-120">For the two sample check formats, the recommended number of slip lines is 17.</span></span> <span data-ttu-id="e9928-121">ولكن، سوف يختلف هذا الرقم، بناءً على مخزون الشيكات لديك، وبرامج تشغيل الطابعة الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="e9928-121">However, this number will vary, depending on your check stock and your printer drivers.</span></span>
- <span data-ttu-id="e9928-122">نوصي بطباعة شيك كاختبار للتحقق من صحة تخطيط الشيك.</span><span class="sxs-lookup"><span data-stu-id="e9928-122">We recommend that you print a test check to validate the check layout.</span></span> <span data-ttu-id="e9928-123">لطباعة شيك اختبار، حدد خيار **اختبار طباعة**.</span><span class="sxs-lookup"><span data-stu-id="e9928-123">To print a test check, select the **Print test** option.</span></span> <span data-ttu-id="e9928-124">تعمل عينات تنسيقات الشيكات بشكل أفضل عندما يتم تعيين الـ **هوامش** إلى **بلا** في خصائص الطابعة المتقدمة لـ Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="e9928-124">The sample check formats work best when **Margins** is set to **None** in the advanced printer properties for Microsoft Excel.</span></span> <span data-ttu-id="e9928-125">بعد إنشاء شيك اختبار، يتم تمكين التحرير مخرجات Excel، وتكوين تخطيط الصفحة بحيث يتم تعيين جميع الهوامش إلى **0** (صفر).</span><span class="sxs-lookup"><span data-stu-id="e9928-125">After the test check has been generated, enable editing of the Excel output, and configure the page layout so that all margins are set to **0** (zero).</span></span> <span data-ttu-id="e9928-126">قم بمقارنة نسخة اختبار الشيك بمخزون الشيكات لديك، ثم قم بضبط الإعدادات حتي تكون راضيًا عن المحاذاة.</span><span class="sxs-lookup"><span data-stu-id="e9928-126">Compare the test copy of the checks to your check stock, and adjust the settings until you're satisfied with the alignment.</span></span>
- <span data-ttu-id="e9928-127">عندما تقوم بإنشاء المدفوعات الخاصة بالحساب البنكي الذي تم تكوينه في دفتر يومية المدفوعات، فسوف تتم طباعة الشيكات باستخدام التنسيق المحدد.</span><span class="sxs-lookup"><span data-stu-id="e9928-127">When you generate payments for the configured bank account in the payment journal, the checks will be printed by using the specified format.</span></span>

<span data-ttu-id="e9928-128">للمزيد من المعلومات، راجع [تعديل تنسيق تقارير إلكترونية](../../dev-itpro/analytics/modify-electronic-reporting-format-reapply-excel-template.md).</span><span class="sxs-lookup"><span data-stu-id="e9928-128">For more information, see [Modify an Electronic reporting format](../../dev-itpro/analytics/modify-electronic-reporting-format-reapply-excel-template.md).</span></span>

