---
title: حالات المستند ودوره الحياة
description: يتناول هذا الموضوع العديد من حالات المستندات المختلفة لعناصر الصفحات في Microsoft Dynamics 365 Commerce.
author: phinneyridge
manager: annbe
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: niholman
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: edb81efc45fc5e7eed32cb7d9b8fda5ade987dd4
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/20/2019
ms.locfileid: "2914877"
---
# <a name="document-states-and-lifecycle"></a><span data-ttu-id="a1770-103">حالات المستند ودوره الحياة</span><span class="sxs-lookup"><span data-stu-id="a1770-103">Document states and lifecycle</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="a1770-104">يتناول هذا الموضوع العديد من حالات المستندات المختلفة لعناصر الصفحات في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="a1770-104">This topic covers the various document states of page elements in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="document-state-descriptions"></a><span data-ttu-id="a1770-105">أوصاف حالة المستند</span><span class="sxs-lookup"><span data-stu-id="a1770-105">Document state descriptions</span></span>

<span data-ttu-id="a1770-106">يسرد الموضوع [عناصر الصفحة](page-elements-overview.md) الأنواع المختلفة من المستندات في نظام إدارة المحتوي (CMS).</span><span class="sxs-lookup"><span data-stu-id="a1770-106">The [Page elements](page-elements-overview.md) topic lists various documents types in the content management system (CMS).</span></span> <span data-ttu-id="a1770-107">يمكن أن يكون لأنواع المستندات العديد من الحالات في أداة التأليف.</span><span class="sxs-lookup"><span data-stu-id="a1770-107">These document types can have several states in the authoring tool.</span></span> <span data-ttu-id="a1770-108">تساعد حالات المستند علي منع تعارض البيانات وفرض التحكم في الإصدار.</span><span class="sxs-lookup"><span data-stu-id="a1770-108">The document states help prevent data conflicts and enforce version control.</span></span> <span data-ttu-id="a1770-109">وهي تحدد من يمكنه تغيير المستندات، ومتى يمكن تغيير المستندات، ومتى يمكن عرض التغييرات بواسطة أشخاص آخرين.</span><span class="sxs-lookup"><span data-stu-id="a1770-109">They determine who can change the documents, when the documents can be changed, and when changes can be viewed by other people.</span></span>

<span data-ttu-id="a1770-110">يوضح الجدول التالي حالات المستند المحتملة لعناصر الصفحة في Commerce.</span><span class="sxs-lookup"><span data-stu-id="a1770-110">The following table shows the possible document states of page elements in Commerce.</span></span>

| <span data-ttu-id="a1770-111">حالة المستند</span><span class="sxs-lookup"><span data-stu-id="a1770-111">Document state</span></span> | <span data-ttu-id="a1770-112">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="a1770-112">Description</span></span> |
|---|---|
| <span data-ttu-id="a1770-113">تم السداد مع الخروج</span><span class="sxs-lookup"><span data-stu-id="a1770-113">Checked out</span></span> | <span data-ttu-id="a1770-114">عندما يتم سحب عنصر CMS إليك، لا يمكن تحريره بواسطة أيًا من مستخدمي النظام المصادقين الآخرين.</span><span class="sxs-lookup"><span data-stu-id="a1770-114">When a CMS item is checked out to you, it can't be edited by any other authenticated system users.</span></span> <span data-ttu-id="a1770-115">وتكون أي تغييرات تُجريها علي العنصر مرئية لك فقط.</span><span class="sxs-lookup"><span data-stu-id="a1770-115">Any changes that you make to the item are visible only to you.</span></span> |
| <span data-ttu-id="a1770-116">تم الإيداع</span><span class="sxs-lookup"><span data-stu-id="a1770-116">Checked in</span></span> | <span data-ttu-id="a1770-117">عند إيداع عنصر CMS، تكون كافة التغييرات مرئية لمستخدمي النظام المصادقين الآخرين، ويمكن لهؤلاء المستخدمين سحب العنصر وتحريره.</span><span class="sxs-lookup"><span data-stu-id="a1770-117">When a CMS item is checked in, all changes are visible to other authenticated system users, and those users can then check out the item and edit it.</span></span> <span data-ttu-id="a1770-118">تقوم كل عمليه إيداع بإنشاء سجل إصدار مستند في سجل الصنف.</span><span class="sxs-lookup"><span data-stu-id="a1770-118">Each check-in creates a document version record in the item's history.</span></span> |
| <span data-ttu-id="a1770-119">منشور</span><span class="sxs-lookup"><span data-stu-id="a1770-119">Published</span></span> | <span data-ttu-id="a1770-120">عند نشر عنصر CMS، يتم نقله إلى موقعك المباشر ويصبح قابلاً للاكتشاف علي الإنترنت بواسطة المستخدمين الخارجيين غير المُصادقين.</span><span class="sxs-lookup"><span data-stu-id="a1770-120">When a CMS item is published, it's pushed to your live site and becomes discoverable on the internet by non-authenticated external users.</span></span> <span data-ttu-id="a1770-121">لا يمكن نشر الأصناف إلا إذا تم إيداعها.</span><span class="sxs-lookup"><span data-stu-id="a1770-121">Items can be published only if they have been checked in.</span></span> |
| <span data-ttu-id="a1770-122">محفوظ</span><span class="sxs-lookup"><span data-stu-id="a1770-122">Saved</span></span> | <span data-ttu-id="a1770-123">يمكن حفظ التغييرات التي تم اجراؤها علي عنصر CMS مسحوب إلى CMS قبل إيداع العنصر أو نشره.</span><span class="sxs-lookup"><span data-stu-id="a1770-123">Changes that have been made to a checked-out CMS item can be saved to the CMS before the item is checked in or published.</span></span> <span data-ttu-id="a1770-124">ولا تظهر هذه التغييرات المحفوظة لمستخدمي النظام المُصادقين الآخرين حتى يتم إيداع العنصر.</span><span class="sxs-lookup"><span data-stu-id="a1770-124">These saved changes aren't visible to other authenticated system users until the item is checked in.</span></span> <span data-ttu-id="a1770-125">و تكون مرئية للمستخدمين الخارجيين إلى أن يتم نشر العنصر.</span><span class="sxs-lookup"><span data-stu-id="a1770-125">They aren't visible to external users until the item is published.</span></span> |
| <span data-ttu-id="a1770-126">تم تجاهل السحب</span><span class="sxs-lookup"><span data-stu-id="a1770-126">Discarded check out</span></span> | <span data-ttu-id="a1770-127">عند تجاهل عنصر CMS تم سحبه، يتم حذف كافة التغييرات المحفوظة، ويتم إرجاع الصنف إلى الإصدار الذي تم إيداعه مؤخرًا.</span><span class="sxs-lookup"><span data-stu-id="a1770-127">When a checked-out CMS item is discarded, all saved changes are deleted, and the item reverts to the version that was most recently checked in.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="a1770-128">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="a1770-128">Additional resources</span></span>

[<span data-ttu-id="a1770-129">طرق إضافة المحتوى</span><span class="sxs-lookup"><span data-stu-id="a1770-129">Ways to add content</span></span>](add-manage-content.md)

[<span data-ttu-id="a1770-130">مصطلحات نموذج الصفحة</span><span class="sxs-lookup"><span data-stu-id="a1770-130">Page model glossary</span></span>](page-elements-overview.md)

[<span data-ttu-id="a1770-131">العمل مع مجموعات النشر</span><span class="sxs-lookup"><span data-stu-id="a1770-131">Work with publish groups</span></span>](publish-groups.md)

[<span data-ttu-id="a1770-132">العمل باستخدام الوحدات النمطية</span><span class="sxs-lookup"><span data-stu-id="a1770-132">Work with modules</span></span>](work-with-modules.md)

[<span data-ttu-id="a1770-133">العمل باستخدام الأجزاء</span><span class="sxs-lookup"><span data-stu-id="a1770-133">Work with fragments</span></span>](work-with-fragments.md)

[<span data-ttu-id="a1770-134">نظرة عامة على القوالب والتخطيطات</span><span class="sxs-lookup"><span data-stu-id="a1770-134">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="a1770-135">تخصيص التنقل في الموقع</span><span class="sxs-lookup"><span data-stu-id="a1770-135">Customize site navigation</span></span>](customize-site-navigation.md)