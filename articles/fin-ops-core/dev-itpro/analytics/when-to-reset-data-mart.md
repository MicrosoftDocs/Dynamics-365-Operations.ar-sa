---
title: الأسئلة المتداولة حول إعادة تعيين متجر البيانات
description: يوفر هذا الموضوع إجابات عن بعض الأسئلة المتداولة حول إعادة تعيين متجر البيانات.
author: jinniew
ms.date: 06/09/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2021-05-06
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 7cd96c7bc698986ef1ef07ca88479a3d49f22924
ms.sourcegitcommit: ecabf43282a3e55f1db40341aa3f3c7950b9e94c
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/16/2021
ms.locfileid: "6266599"
---
# <a name="data-mart-resets-faq"></a><span data-ttu-id="32c09-103">الأسئلة المتداولة حول إعادة تعيين متجر البيانات</span><span class="sxs-lookup"><span data-stu-id="32c09-103">Data mart resets FAQ</span></span>

<span data-ttu-id="32c09-104">يوفر هذا الموضوع إجابات عن بعض الأسئلة المتداولة حول إعادة تعيين متجر البيانات.</span><span class="sxs-lookup"><span data-stu-id="32c09-104">This topic provides answers to some frequently asked questions about data mart resets.</span></span> <span data-ttu-id="32c09-105">يمكن لا تكون إعادة تعيين متجر البيانات عملية تستغرق وقتًا طويلاً، وفقًا للظروف، الحل المطلوب.</span><span class="sxs-lookup"><span data-stu-id="32c09-105">A reset of the data mart can be a time-consuming process and, depending on the circumstances, might not be the solution that is required.</span></span> <span data-ttu-id="32c09-106">وبالتالي، يتضمن هذا الموضوع معلومات حول الظروف التي قد يساعد فيها إعادة تعيين متجر البيانات وكذلك الظروف التي من غير المحتمل أن تساعد.</span><span class="sxs-lookup"><span data-stu-id="32c09-106">Therefore, this topic includes information about circumstances where a data mart reset might help and also circumstances where it's unlikely to help.</span></span>

## <a name="what-is-a-data-mart-reset"></a><span data-ttu-id="32c09-107">ما وقت إعادة تعيين متجر البيانات؟</span><span class="sxs-lookup"><span data-stu-id="32c09-107">What is a data mart reset?</span></span>

<span data-ttu-id="32c09-108">ستعمل إعادة تعيين متجر البيانات على تعطيل مهام التكامل، وحذف كافة بيانات متجر البيانات، ثم إعادة تمكين التكامل.</span><span class="sxs-lookup"><span data-stu-id="32c09-108">A data mart reset will disable the integration tasks, delete all the data mart data, and then re-enable integration.</span></span>

<span data-ttu-id="32c09-109">للتأكد من أن البيانات القديمة لم يتم إدراجها، يمكن بدء إعادة تعيين متجر البيانات بعد إكمال المهام الموجودة.</span><span class="sxs-lookup"><span data-stu-id="32c09-109">To ensure that old data isn't inserted, a data mart reset can be started only after existing tasks are completed.</span></span> <span data-ttu-id="32c09-110">إذا حاولت إعادة تعيين متجر البيانات قبل اكتمال كافة المهام، فقد تتلقي رسالة مثل، "تعذر معالجة إعادة تعيين متجر البيانات بسبب المهمة النشطة.</span><span class="sxs-lookup"><span data-stu-id="32c09-110">If you try to reset the data mart before all tasks are completed, you might receive a message such as, "The data mart reset was unable to be processed because of an active task.</span></span> <span data-ttu-id="32c09-111">الرجاء المحاولة مره أخرى لاحقا."</span><span class="sxs-lookup"><span data-stu-id="32c09-111">Please try again later."</span></span>

## <a name="when-do-i-have-to-do-a-data-mart-reset"></a><span data-ttu-id="32c09-112">متى يجب أن يقوم بإعادة تعيين متجر بيانات؟</span><span class="sxs-lookup"><span data-stu-id="32c09-112">When do I have to do a data mart reset?</span></span>

<span data-ttu-id="32c09-113">في حالة تطبيق واحدة أو أكثر من الكشوف التالية على الحالة الخاصة بك، يمكن لمؤسسك الاستفادة من إعادة تعيين متجر البيانات:</span><span class="sxs-lookup"><span data-stu-id="32c09-113">If one or more of the following statements apply to your situation, your organization can benefit from a data mart reset:</span></span>

- <span data-ttu-id="32c09-114">تمت استعادة قاعدة بيانات التطبيق.</span><span class="sxs-lookup"><span data-stu-id="32c09-114">The application database was restored.</span></span>
- <span data-ttu-id="32c09-115">لقد قمت بفتح تذكرة دعم وقام مهندس دعم بإرشادك لإعادة تعيين متجر البيانات كجزء من خطوة استكشاف الأخطاء وإصلاحها.</span><span class="sxs-lookup"><span data-stu-id="32c09-115">You opened a support ticket, and a Support engineer instructed you to reset the data mart as part of a troubleshooting step.</span></span>
 
## <a name="when-is-a-data-mart-reset-inappropriate"></a><span data-ttu-id="32c09-116">متى يكون إعادة تعيين متجر بيانات غير مناسب؟</span><span class="sxs-lookup"><span data-stu-id="32c09-116">When is a data mart reset inappropriate?</span></span>

<span data-ttu-id="32c09-117">إليك بعض الحالات حيث لا نُوصي بإعادة تعيين متجر البيانات:</span><span class="sxs-lookup"><span data-stu-id="32c09-117">Here are some of the circumstances where we don't recommend that you reset the data mart:</span></span>

- <span data-ttu-id="32c09-118">مواجهة مشكلات في الأداء مقترنة بمزامنة البيانات.</span><span class="sxs-lookup"><span data-stu-id="32c09-118">You're experiencing performance issues that are associated with data synchronization.</span></span>
- <span data-ttu-id="32c09-119">لديك نقش إعادة تعيين متكرر لأي من الأسباب التالية:</span><span class="sxs-lookup"><span data-stu-id="32c09-119">You have a recurring reset pattern for any of the following reasons:</span></span>

    - <span data-ttu-id="32c09-120">**البيانات المفقودة** – إذا لاحظت أن البيانات مفقودة، فافتح تذكرة دعم مع Microsoft لمراجعة تنسيق التقرير الخاص بك وكذلك المشكلات المحتملة لمزامنة البيانات.</span><span class="sxs-lookup"><span data-stu-id="32c09-120">**Missing data** – If you notice that data is missing, open a support ticket with Microsoft to review your report format and possible data synchronization issues.</span></span>
    - <span data-ttu-id="32c09-121">**حالة التكامل العالق**</span><span class="sxs-lookup"><span data-stu-id="32c09-121">**Stuck integration state**</span></span>
    - <span data-ttu-id="32c09-122">**السجلات القديمة** – لا تعمل السجلات التالفة نفسها على تبرير إعادة تعيين متجر البيانات بالضرورة.</span><span class="sxs-lookup"><span data-stu-id="32c09-122">**Stale records** – Stale records by themselves don't necessarily justify a data mart reset.</span></span> <span data-ttu-id="32c09-123">إذا كانت لديك مجموعة كبيرة من البيانات، ستتطلب عملية إعادة التعيين بعض الوقت ليتم تشغيلها، ولكنها من المحتمل أن تؤدي إلى أي تحسين.</span><span class="sxs-lookup"><span data-stu-id="32c09-123">If you have a large data set, the reset process will take some time to run but is unlikely to lead to any improvement.</span></span>

## <a name="if-i-reset-the-data-mart-will-i-lose-reports-that-ive-already-designed"></a><span data-ttu-id="32c09-124">إذا قمت باعادة تعيين متجر البيانات، فهل ستفقد التقارير التي قمت بتصميمها بالفعل؟</span><span class="sxs-lookup"><span data-stu-id="32c09-124">If I reset the data mart, will I lose reports that I've already designed?</span></span>

<span data-ttu-id="32c09-125">الرقم</span><span class="sxs-lookup"><span data-stu-id="32c09-125">No.</span></span> <span data-ttu-id="32c09-126">يتم تخزين التقارير الخاصة بك في جداول SQL التي لا تتأثر بإعادة تعيين متجر البيانات.</span><span class="sxs-lookup"><span data-stu-id="32c09-126">Your reports are stored in SQL tables that aren't affected by a data mart reset.</span></span> <span data-ttu-id="32c09-127">إذا كنت مهتمًا بفقدان تقارير قمت بتصميمها، يمكنك إجراء النسخ الاحتياطي للتصميمات التي لا ترغب في فقدها.</span><span class="sxs-lookup"><span data-stu-id="32c09-127">If you're concerned about losing reports that you've designed, you can back up the designs that you don't want to lose.</span></span> <span data-ttu-id="32c09-128">لنسخ التصميمات احتياطيًا، افتح Report Designer، وانتقل إلى **الشركة \> الشركات \> كتل الإنشاء \> تصدير**.</span><span class="sxs-lookup"><span data-stu-id="32c09-128">To back up designs, open Report Designer, and go to **Company \> Companies \> Building Blocks \> Export**.</span></span>
 
## <a name="do-all-users-have-to-exit-the-system-before-i-can-reset-the-data-mart"></a><span data-ttu-id="32c09-129">هل يتعين على كافة المستخدمين الخروج من النظام قبل أن أقوم بإعادة تعيين متجر البيانات؟</span><span class="sxs-lookup"><span data-stu-id="32c09-129">Do all users have to exit the system before I can reset the data mart?</span></span>

<span data-ttu-id="32c09-130">الرقم</span><span class="sxs-lookup"><span data-stu-id="32c09-130">No.</span></span> <span data-ttu-id="32c09-131">يمكن للمستخدمين متابعة العمل في النظام أثناء إعادة تعيين متجر البيانات.</span><span class="sxs-lookup"><span data-stu-id="32c09-131">Users can continue to work in the system during a data mart reset.</span></span> <span data-ttu-id="32c09-132">ومع ذلك، حتى يتم إكمال إعادة التعيين، لن يتمكن المستخدمون من الوصول إلى أية تقارير تم إنشاؤها باستخدام Financial Reporter.</span><span class="sxs-lookup"><span data-stu-id="32c09-132">However, until the reset is completed, users won't be able to access any reports that were created by using Financial Reporter.</span></span>

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
