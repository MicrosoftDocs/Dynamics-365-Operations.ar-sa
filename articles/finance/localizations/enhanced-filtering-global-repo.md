---
title: تصفية RCS المحسنة في RCS/المستودع العمومي
description: يصف هذا الموضوع قدرات التصفية المحسنة للمستودع العمومي RCS، التي تم تحسينها لتضمين عوامل تصفية إضافية.
author: JaneA07
manager: AnnBe
ms.date: 04/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, ERWorkspace
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: a67a4345271cbeffc100fc1d9077cc866846a4d4
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "5005832"
---
# <a name="rcs-enhanced-filtering-options-for-finding-configurations-in-the-rcsglobal-repository"></a><span data-ttu-id="ccd67-103">خيارات تصفية RCS المحسنة للبحث عن التكوينات في RCS/المستودع العمومي</span><span class="sxs-lookup"><span data-stu-id="ccd67-103">RCS enhanced filtering options for finding configurations in the RCS/Global repository</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ccd67-104">يصف هذا الموضوع قدرات التصفية المحسنة للمستودع العمومي لخدمات Regulatory Configuration Services (RCS)، التي تم تحسينها لتشمل القدرة على التصفية باستخدام العوامل التالية:</span><span class="sxs-lookup"><span data-stu-id="ccd67-104">This topic describes enhanced filtering capabilities for Regulatory Configuration Services (RCS) Global repository, which have been improved to include the ability to filter with the following criteria:</span></span> 
- <span data-ttu-id="ccd67-105">**البلد/المنطقة** - بالاستناد إلى أكواد بلدان ISO</span><span class="sxs-lookup"><span data-stu-id="ccd67-105">**Country/region** - Based on ISO country codes</span></span>  
- <span data-ttu-id="ccd67-106">أنواع **العلامات** لـ:</span><span class="sxs-lookup"><span data-stu-id="ccd67-106">**Tags** types for:</span></span>
  - <span data-ttu-id="ccd67-107">المنطقة الوظيفية</span><span class="sxs-lookup"><span data-stu-id="ccd67-107">Functional area</span></span>
  - <span data-ttu-id="ccd67-108">منطقة الميزة</span><span class="sxs-lookup"><span data-stu-id="ccd67-108">Feature area</span></span>
  - <span data-ttu-id="ccd67-109">المجال</span><span class="sxs-lookup"><span data-stu-id="ccd67-109">Industry</span></span> 
  - <span data-ttu-id="ccd67-110">مستند الأعمال</span><span class="sxs-lookup"><span data-stu-id="ccd67-110">Business document</span></span> 

<span data-ttu-id="ccd67-111">لتسهيل اكتشاف تكوينات خاصة أو متعلقة يمكنك تطبيق عوامل التصفية، إما بشكل فردي أو كمجموعة.</span><span class="sxs-lookup"><span data-stu-id="ccd67-111">To make it easier to discover specific or related configurations you can apply filters, either individually or as a group.</span></span> <span data-ttu-id="ccd67-112">على سبيل المثال، للعثور على نوع واحد من 'مستندات الأعمال القابلة للتكوين المرتبطة بفواتير المورد، يمكنك تطبيق عامل التصفية **نوع مستند الأعمال** للبحث عن هذا النوع من المستندات.</span><span class="sxs-lookup"><span data-stu-id="ccd67-112">For example, to find a single type of 'configurable business documents that are related to vendor invoices, you could apply a **Business document type** filter to search for that type of document.</span></span> 

<span data-ttu-id="ccd67-113">[![قسام عامل التصفية للمستودع العام](media/rcs-enhanced-filter-section.JPG)](./media/rcs-enhanced-filter-section.JPG)</span><span class="sxs-lookup"><span data-stu-id="ccd67-113">[![Filter section for Global repository](media/rcs-enhanced-filter-section.JPG)](./media/rcs-enhanced-filter-section.JPG)</span></span> 

<span data-ttu-id="ccd67-114">يمكنك إجراء مزيد من التنقيح في البحث بتحديد نوع المستند، على سبيل المثال 'فاتورة المورد' والنقر فوق **تطبيق عامل التصفية**.</span><span class="sxs-lookup"><span data-stu-id="ccd67-114">You can further refine the search by selecting document type, for example 'vendor invoice' and clicking **Apply filter**.</span></span> <span data-ttu-id="ccd67-115">يبين المثال التالي النتائج عند إجراء التصفية على **نوع مستند الأعمال** مع نوع المستند المضاف.</span><span class="sxs-lookup"><span data-stu-id="ccd67-115">The following example shows the results when filtering on **Business document type** with the document type added.</span></span> 

<span data-ttu-id="ccd67-116">[![تطبيق عامل التصفية والاستيراد لنوع مستند الاعمال](media/rcs-enhanced-filtering-applied.JPG)](./media/rcs-enhanced-filtering-applied.JPG)</span><span class="sxs-lookup"><span data-stu-id="ccd67-116">[![Applied filter and Import for business document type](media/rcs-enhanced-filtering-applied.JPG)](./media/rcs-enhanced-filtering-applied.JPG)</span></span> 

<span data-ttu-id="ccd67-117">يمكن استيراد النتائج المصفاة إلى مستودع RCS للمستخدمين أو بيئة Dynamics 365 Finance، سواء بشكل فردي أو كمجموعة.</span><span class="sxs-lookup"><span data-stu-id="ccd67-117">Filtered results can be imported into a users RCS repository or a Dynamics 365 Finance environment, either individually or as a set.</span></span> <span data-ttu-id="ccd67-118">للقيام بذلك، حدد مجموعة التكوينات، وانقر فوق **استيراد**.</span><span class="sxs-lookup"><span data-stu-id="ccd67-118">To do this, select the group of configurations, and click **Import**.</span></span>
