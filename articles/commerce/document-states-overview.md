---
title: حالات المستند ودوره الحياة
description: يتناول هذا الموضوع العديد من حالات المستندات المختلفة لعناصر الصفحات في Microsoft Dynamics 365 Commerce.
author: phinneyridge
manager: annbe
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: niholman
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 457b1ac7afb8cad57399572acf429d208db917af
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5230524"
---
# <a name="document-states-and-lifecycle"></a><span data-ttu-id="c99af-103">حالات المستند ودورة الحياة</span><span class="sxs-lookup"><span data-stu-id="c99af-103">Document states and lifecycle</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="c99af-104">يتناول هذا الموضوع العديد من حالات المستندات المختلفة لعناصر الصفحات في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="c99af-104">This topic covers the various document states of page elements in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="document-state-descriptions"></a><span data-ttu-id="c99af-105">أوصاف حالة المستند</span><span class="sxs-lookup"><span data-stu-id="c99af-105">Document state descriptions</span></span>

<span data-ttu-id="c99af-106">يسرد الموضوع [عناصر الصفحة](page-elements-overview.md) الأنواع المختلفة من المستندات في نظام إدارة المحتوي (CMS).</span><span class="sxs-lookup"><span data-stu-id="c99af-106">The [Page elements](page-elements-overview.md) topic lists various documents types in the content management system (CMS).</span></span> <span data-ttu-id="c99af-107">يمكن أن يكون لأنواع المستندات العديد من الحالات في أداة التأليف.</span><span class="sxs-lookup"><span data-stu-id="c99af-107">These document types can have several states in the authoring tool.</span></span> <span data-ttu-id="c99af-108">تساعد حالات المستند علي منع تعارض البيانات وفرض التحكم في الإصدار.</span><span class="sxs-lookup"><span data-stu-id="c99af-108">The document states help prevent data conflicts and enforce version control.</span></span> <span data-ttu-id="c99af-109">وهي تحدد من يمكنه تغيير المستندات، ومتى يمكن تغيير المستندات، ومتى يمكن عرض التغييرات بواسطة أشخاص آخرين.</span><span class="sxs-lookup"><span data-stu-id="c99af-109">They determine who can change the documents, when the documents can be changed, and when changes can be viewed by other people.</span></span>

<span data-ttu-id="c99af-110">يوضح الجدول التالي حالات المستند المحتملة لعناصر الصفحة في Commerce.</span><span class="sxs-lookup"><span data-stu-id="c99af-110">The following table shows the possible document states of page elements in Commerce.</span></span>

| <span data-ttu-id="c99af-111">حالة المستند</span><span class="sxs-lookup"><span data-stu-id="c99af-111">Document state</span></span>      | <span data-ttu-id="c99af-112">إجراء منشئ الموقع</span><span class="sxs-lookup"><span data-stu-id="c99af-112">Site builder action</span></span>        | <span data-ttu-id="c99af-113">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="c99af-113">Description</span></span>                                                  |
| ------------------- | -------------------------- | ------------------------------------------------------------ |
| <span data-ttu-id="c99af-114">تم السحب</span><span class="sxs-lookup"><span data-stu-id="c99af-114">Checked out</span></span>         | <span data-ttu-id="c99af-115">حدد **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="c99af-115">Select **Edit**.</span></span>           | <span data-ttu-id="c99af-116">يتم سحب المستند المطلوب لك.</span><span class="sxs-lookup"><span data-stu-id="c99af-116">The applicable document is checked out to you.</span></span> <span data-ttu-id="c99af-117">بينما يكون المستند في هذه الحالة، لا يمكن تغييره من قبل مستخدمي النظام الآخرين المصادق عليهم، وستكون أي تغييرات تجريها على المستند مرئية لك فقط.</span><span class="sxs-lookup"><span data-stu-id="c99af-117">While a document is in this state, it can't be changed by other authenticated system users, and any changes that you make to the document are visible only to you.</span></span> |
| <span data-ttu-id="c99af-118">محفوظ</span><span class="sxs-lookup"><span data-stu-id="c99af-118">Saved</span></span>               | <span data-ttu-id="c99af-119">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="c99af-119">Select **Save**.</span></span>           | <span data-ttu-id="c99af-120">يتم حفظ التغييرات التي تم اجراؤها على مستند مسحوب في قاعدة البيانات، ولكن لم يتم بعد إيداع المستند أو نشره.</span><span class="sxs-lookup"><span data-stu-id="c99af-120">Changes that have been made to a checked-out document are saved to the database, but the document isn't yet checked in or published.</span></span> <span data-ttu-id="c99af-121">لا تظهر التغييرات المحفوظة لمستخدمي النظام المُصادقين الآخرين حتى يحدد الكاتب **إنهاء التحرير**.</span><span class="sxs-lookup"><span data-stu-id="c99af-121">The saved changes aren't visible to other authenticated system users until the author selects **Finish editing**.</span></span> <span data-ttu-id="c99af-122">و تكون مرئية للمستخدمين الخارجيين إلى أن يتم نشر العنصر.</span><span class="sxs-lookup"><span data-stu-id="c99af-122">They aren't visible to external users until the item is published.</span></span> |
| <span data-ttu-id="c99af-123">تم تجاهل السحب</span><span class="sxs-lookup"><span data-stu-id="c99af-123">Discarded check out</span></span> | <span data-ttu-id="c99af-124">حدد **تجاهل عمليات التحرير**.</span><span class="sxs-lookup"><span data-stu-id="c99af-124">Select **Discard edits**.</span></span>  | <span data-ttu-id="c99af-125">يتم تجاهل كافة التغييرات التي تم إدخالها على المستند المسحوب، ويعود العنصر إلى الإصدار الأخير الذي تم إيداعه.</span><span class="sxs-lookup"><span data-stu-id="c99af-125">All changes to the checked-out document are discarded, and the item reverts to the last version that was checked in.</span></span> |
| <span data-ttu-id="c99af-126">تم الإيداع</span><span class="sxs-lookup"><span data-stu-id="c99af-126">Checked in</span></span>          | <span data-ttu-id="c99af-127">حدد **إنهاء التحرير**.</span><span class="sxs-lookup"><span data-stu-id="c99af-127">Select **Finish editing**.</span></span> | <span data-ttu-id="c99af-128">يتم إيداع المستند المحرر.</span><span class="sxs-lookup"><span data-stu-id="c99af-128">The edited document is checked in.</span></span> <span data-ttu-id="c99af-129">تكون كافة التغييرات مرئية لمستخدمي النظام المصادقين الآخرين، ويمكن لهؤلاء المستخدمين عندئذٍ تحرير المستند.</span><span class="sxs-lookup"><span data-stu-id="c99af-129">All changes are visible to other authenticated system users, and those users can then edit the document.</span></span> <span data-ttu-id="c99af-130">تقوم كل عمليه إيداع بإنشاء سجل إصدار مستند في سجل الصنف.</span><span class="sxs-lookup"><span data-stu-id="c99af-130">Each check-in creates a document version record in the item's history.</span></span> |
| <span data-ttu-id="c99af-131">منشور</span><span class="sxs-lookup"><span data-stu-id="c99af-131">Published</span></span>           | <span data-ttu-id="c99af-132">حدد **نشر**.</span><span class="sxs-lookup"><span data-stu-id="c99af-132">Select **Publish**.</span></span>        | <span data-ttu-id="c99af-133">يتم نشر المستند، ويتم دفع التغييرات إلى موقعك المباشر وتصبح قابلة للاكتشاف بواسطة مستخدمين خارجيين.</span><span class="sxs-lookup"><span data-stu-id="c99af-133">The document is published, and the changes are pushed to your live site and become discoverable by external users.</span></span> <span data-ttu-id="c99af-134">لا يمكن نشر العناصر الا إذا تم إيداعها أولاً من خلال تحديد **إنهاء التحرير**.</span><span class="sxs-lookup"><span data-stu-id="c99af-134">Items can be published only if they have first been checked in by selecting **Finish editing**.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="c99af-135">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="c99af-135">Additional resources</span></span>

[<span data-ttu-id="c99af-136">طرق إضافة المحتوى</span><span class="sxs-lookup"><span data-stu-id="c99af-136">Ways to add content</span></span>](add-manage-content.md)

[<span data-ttu-id="c99af-137">مصطلحات نموذج الصفحة</span><span class="sxs-lookup"><span data-stu-id="c99af-137">Page model glossary</span></span>](page-elements-overview.md)

[<span data-ttu-id="c99af-138">العمل مع مجموعات النشر</span><span class="sxs-lookup"><span data-stu-id="c99af-138">Work with publish groups</span></span>](publish-groups.md)

[<span data-ttu-id="c99af-139">تمكين المشاركة عبر القنوات واستخدامها</span><span class="sxs-lookup"><span data-stu-id="c99af-139">Enable and use cross-channel sharing</span></span>](cross-channel-sharing.md)

[<span data-ttu-id="c99af-140">العمل باستخدام الوحدات النمطية</span><span class="sxs-lookup"><span data-stu-id="c99af-140">Work with modules</span></span>](work-with-modules.md)

[<span data-ttu-id="c99af-141">العمل باستخدام الأجزاء</span><span class="sxs-lookup"><span data-stu-id="c99af-141">Work with fragments</span></span>](work-with-fragments.md)

[<span data-ttu-id="c99af-142">نظرة عامة على القوالب والتخطيطات</span><span class="sxs-lookup"><span data-stu-id="c99af-142">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="c99af-143">تخصيص التنقل في الموقع</span><span class="sxs-lookup"><span data-stu-id="c99af-143">Customize site navigation</span></span>](customize-site-navigation.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]