---
title: "كتالوجات مركز الاتصال"
description: "توضح هذه المقالة الوظائف الخاصة بمركز الاتصال للكتالوجات في Microsoft Dynamics 365 for Retail."
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 16231
ms.assetid: f28a827c-3a50-4d5e-83eb-e5a768db70a1
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 7be87496ceaea2d1d5f97a5cc17e50dcddbaf33d
ms.contentlocale: ar-sa
ms.lasthandoff: 09/29/2017

---

# <a name="call-center-catalogs"></a><span data-ttu-id="52763-103">كتالوجات مركز الاتصال</span><span class="sxs-lookup"><span data-stu-id="52763-103">Call center catalogs</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="52763-104">توضح هذه المقالة الوظائف الخاصة بمركز الاتصال للكتالوجات في Microsoft Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="52763-104">This article describes the call center–specific functionality for catalogs in Microsoft Dynamics 365 for Retail.</span></span>

<span data-ttu-id="52763-105">في مركز الاتصال، يمكنك استخدام كتالوجات منتجات لتحديد المنتجات التي تريد عرضها للعملاء.</span><span class="sxs-lookup"><span data-stu-id="52763-105">In a call center, you can use product catalogs to identify the products that you want to offer to customers.</span></span> <span data-ttu-id="52763-106">عادة، تستخدم مراكز الاتصال الكتالوجات المطبوعة.</span><span class="sxs-lookup"><span data-stu-id="52763-106">Call centers typically use printed catalogs.</span></span> <span data-ttu-id="52763-107">تتم معالجة تصميم وإنتاج الكتالوجات المطبوعة خارج Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="52763-107">The design and production of a printed catalog is handled outside Dynamics 365 for Retail.</span></span> <span data-ttu-id="52763-108">ومع ذلك، يمكنك إنشاء وتخزين نموذج رقمي لكتالوج باستخدام نفس الصفحات التي استخدمتها لإعداد كتالوجات البيع بالتجزئة على الإنترنت.</span><span class="sxs-lookup"><span data-stu-id="52763-108">However, you can create and store a digital form of a catalog by using the same pages that you use to set up online retail catalogs.</span></span> <span data-ttu-id="52763-109">قبل إنشاء كتالوج، يجب إعداد عمليات فرز المنتجات وتعيين عمليات الفرز إلى مركز اتصال.</span><span class="sxs-lookup"><span data-stu-id="52763-109">Before you can create a catalog, you must set up product assortments and assign the assortments to a call center.</span></span> <span data-ttu-id="52763-110">يمكنك أيضا إضافة منتجات إلى الكتالوج من خلال تحديد المنتجات من عمليات الفرز هذه.</span><span class="sxs-lookup"><span data-stu-id="52763-110">You then add products to the catalog by selecting products from these assortments.</span></span> <span data-ttu-id="52763-111">بعد إضافة المنتجات إلى الكتالوج واكتمال الكتالوج، يجب التحقق من صحة الكتالوج للتحقق من البيانات.</span><span class="sxs-lookup"><span data-stu-id="52763-111">After products have been added to the catalog, and the catalog is complete, you must validate the catalog to verify the data.</span></span> <span data-ttu-id="52763-112">ثم يجب إرسال الكتالوج لمراجعته واعتماده.</span><span class="sxs-lookup"><span data-stu-id="52763-112">You must then submit the catalog for review and approval.</span></span> <span data-ttu-id="52763-113">وبعد الموافقة على الكتالوج، يمكن نشره.</span><span class="sxs-lookup"><span data-stu-id="52763-113">After the catalog is approved, it can be published.</span></span> <span data-ttu-id="52763-114">عندما يتم إنشاء كتالوج مركز الاتصال، يمكنك أخذ لقطة من بيانات الكتالوج في الوقت الذي يتم نشر الكتالوج فيه.</span><span class="sxs-lookup"><span data-stu-id="52763-114">When a call center catalog is created, you can take a snapshot of the catalog data at the time that the catalog is published.</span></span> <span data-ttu-id="52763-115">تتيح لك وظيفة اللقطة هذه الوصول إلى إصدار معين من الكتالوج حتى في حالة تغيير الكتالوج وتحديثه لاحقاً.</span><span class="sxs-lookup"><span data-stu-id="52763-115">This snapshot functionality lets you access a particular version of the catalog even if the catalog is later changed and updated.</span></span> <span data-ttu-id="52763-116">يمكن أيضا إعداد كتالوجات مركز الاتصال لتتضمن الميزات الاختيارية التالية:</span><span class="sxs-lookup"><span data-stu-id="52763-116">Call center catalogs can also be set up to include the following optional features:</span></span>

-   <span data-ttu-id="52763-117">**رموز المصدر** – رموز المصدر المستخدمة لتعقب استجابة العملاء للمراسلات البريدية لكتالوج معين.</span><span class="sxs-lookup"><span data-stu-id="52763-117">**Source codes** – Source codes are used to track the customer response to specific catalog mailings.</span></span>
-   <span data-ttu-id="52763-118">**المنتجات المجانية** - يمكن تضمين المنتجات في أمر العميل بدون تكلفة إضافية.</span><span class="sxs-lookup"><span data-stu-id="52763-118">**Free products** – Products can be included in a customer's order at no additional charge.</span></span> <span data-ttu-id="52763-119">وتتم إضافة هذه المنتجات إلى الأمر تلقائياً عند إدخال التعليمات البرمجية المصدر للكتالوج في الأمر.</span><span class="sxs-lookup"><span data-stu-id="52763-119">These products are automatically added to an order when the source code for the catalog is entered into the order.</span></span>
-   <span data-ttu-id="52763-120">**البرامج النصية** – النصوص التي يقوم عامل مركز الاتصال بقرائتها للعميل عند إنشاء أمر مبيعات.</span><span class="sxs-lookup"><span data-stu-id="52763-120">**Scripts** – Scripts are texts that a call center worker reads to a customer when a sales order is being created.</span></span> <span data-ttu-id="52763-121">يمكن أن تتضمن البرامج النصية التهاني أو اقتراحات الشراء.</span><span class="sxs-lookup"><span data-stu-id="52763-121">Scripts can include greetings or purchase suggestions.</span></span>
-   <span data-ttu-id="52763-122">**تخطيط الصفحة** – تخطيط صفحة يلتقط موضع صفحة المنتجات في كتالوج مطبوع.</span><span class="sxs-lookup"><span data-stu-id="52763-122">**Page layout** – A page layout captures the page position of products in the printed catalog.</span></span> <span data-ttu-id="52763-123">يتم استخدام هذه المعلومات لتقرير تحليل منطقة الكتالوج.</span><span class="sxs-lookup"><span data-stu-id="52763-123">This information is used for the catalog area analysis report.</span></span>





