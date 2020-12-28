---
title: محفوظات أحداث الأصول
description: يشرح هذا الموضوع كيفية الوصول إلى محفوظات أحداث الأصول في إدارة الأصول.
author: josaw1
manager: tfehr
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 25d53b1380887789c6c4a7a51b600dccfe4589f5
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/13/2020
ms.locfileid: "4421501"
---
# <a name="asset-event-history"></a><span data-ttu-id="00160-103">محفوظات أحداث الأصول</span><span class="sxs-lookup"><span data-stu-id="00160-103">Asset event history</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="00160-104">يشرح هذا الموضوع كيفية الوصول إلى محفوظات أحداث الأصول في إدارة الأصول.</span><span class="sxs-lookup"><span data-stu-id="00160-104">This topic explains how to access asset event history in Asset Management.</span></span> <span data-ttu-id="00160-105">تعرض صفحة‏‎ **محفوظات أحداث الأصول** محفوظات التسجيل التي تم إنشاؤها خلال فترة عمل الأصل.</span><span class="sxs-lookup"><span data-stu-id="00160-105">The **Asset event history** page shows the registration history that has been made during the lifetime of an asset.</span></span> <span data-ttu-id="00160-106">يمكنك الوصول إلى هذه الصفحة من بنود القائمة **كل الأصول‏‎** و **الأصول النشطة‏‎** و **أصولي النشطة**.</span><span class="sxs-lookup"><span data-stu-id="00160-106">You can access this page from the **All assets**, **Active assets**, and **My active assets** menu items.</span></span> <span data-ttu-id="00160-107">حدد أصلاً، ثم حدد **محفوظات الأحداث**.</span><span class="sxs-lookup"><span data-stu-id="00160-107">Select an asset, and then select **Event history**.</span></span>

<span data-ttu-id="00160-108">على علامة التبويب السريعة **التفاصيل‏‎** في صفحة **محفوظات أحداث الأصول**، يمكنك إجراء بحث على جميع المعلومات المتوفرة.</span><span class="sxs-lookup"><span data-stu-id="00160-108">On the **Details** FastTab of the **Asset event history** page, you can do a search on all the available information.</span></span> <span data-ttu-id="00160-109">على سبيل المثال، يمكنك استخدام محفوظات أحداث الأصول للعثور على المعلومات التالية:</span><span class="sxs-lookup"><span data-stu-id="00160-109">For example, you can use the asset event history to find the following information:</span></span>

- <span data-ttu-id="00160-110">تاريخ ووقت آخر استخدام لنوع وظيفة على أحد الأصول</span><span class="sxs-lookup"><span data-stu-id="00160-110">When a job type was last used on an asset</span></span>
- <span data-ttu-id="00160-111">تاريخ ووقت قيام عامل بإدخال ملاحظة حول وظيفة أمر عمل</span><span class="sxs-lookup"><span data-stu-id="00160-111">When a specific worker entered a remark on a work order job</span></span>

<span data-ttu-id="00160-112">يتم تحديث المخطط الزمني في كل مرة يتم فيها فتح الصفحة.</span><span class="sxs-lookup"><span data-stu-id="00160-112">The timeline is updated every time that the page is opened.</span></span> <span data-ttu-id="00160-113">وهو يحتوي على المعلومات التالية:</span><span class="sxs-lookup"><span data-stu-id="00160-113">It contains the following information:</span></span>

- <span data-ttu-id="00160-114">التغييرات التي تم إدخالها على الأصل: موقع الأصل ومعرف الأصل والاسم وضمان المورّد</span><span class="sxs-lookup"><span data-stu-id="00160-114">Changes that have been made on the asset: asset location, asset ID, name, and vendor warranty</span></span>
- <span data-ttu-id="00160-115">الأصل الأساسي</span><span class="sxs-lookup"><span data-stu-id="00160-115">Asset parent</span></span>
- <span data-ttu-id="00160-116">قائمة مكونات الصنف للأصل</span><span class="sxs-lookup"><span data-stu-id="00160-116">Asset bill of materials (BOM)</span></span>
- <span data-ttu-id="00160-117">سجل حالة دورة حياة الأصل</span><span class="sxs-lookup"><span data-stu-id="00160-117">Asset lifecycle state log</span></span>
- <span data-ttu-id="00160-118">موقع العمل</span><span class="sxs-lookup"><span data-stu-id="00160-118">Functional location</span></span>
- <span data-ttu-id="00160-119">طلبات الصيانة</span><span class="sxs-lookup"><span data-stu-id="00160-119">Maintenance requests</span></span>
- <span data-ttu-id="00160-120">أوامر العمل، بما في ذلك الأصناف المرحلة والملاحظات</span><span class="sxs-lookup"><span data-stu-id="00160-120">Work orders, including posted item and notes</span></span>
- <span data-ttu-id="00160-121">الأخطاء</span><span class="sxs-lookup"><span data-stu-id="00160-121">Faults</span></span>
- <span data-ttu-id="00160-122">تقييمات الحالة</span><span class="sxs-lookup"><span data-stu-id="00160-122">Condition assessments</span></span>
