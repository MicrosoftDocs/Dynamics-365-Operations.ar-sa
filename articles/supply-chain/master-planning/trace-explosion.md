---
title: استخدام التتبع لعملية تحديد إجمالي المكونات المطلوبة‬
description: تشرح هذه المقالة كيفية استخدام التتبع لاستكشاف الأسباب الكامنة وراء نتائج إجمالي المكونات المطلوبة للأمر.
author: roxanadiaconu
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqTransExplosion
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 19231
ms.assetid: 9bc9bfbe-a7a9-437b-a947-826229b0585a
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 046d4f5270869542d33023b9b9c927e89f5ad40b
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/02/2020
ms.locfileid: "3209503"
---
# <a name="use-tracing-for-explosion"></a><span data-ttu-id="9de02-103">استخدام التتبع لعملية تحديد إجمالي المكونات المطلوبة‬</span><span class="sxs-lookup"><span data-stu-id="9de02-103">Use tracing for explosion</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9de02-104">تشرح هذه المقالة كيفية استخدام التتبع لاستكشاف الأسباب الكامنة وراء نتائج إجمالي المكونات المطلوبة للأمر.</span><span class="sxs-lookup"><span data-stu-id="9de02-104">This article explains how you can use tracing to explore the causes behind the outcome of an order explosion.</span></span>

<span data-ttu-id="9de02-105">بواسطة تمكين التتبع، يمكنك عرض معلومات حول العوامل التي ساهمت في نتيجة تحديد إجمالي المكونات المطلوبة لأمر معين.</span><span class="sxs-lookup"><span data-stu-id="9de02-105">By enabling tracing, you can view information about the factors that contributed to the outcome of the explosion of a particular order.</span></span> <span data-ttu-id="9de02-106">توضح الأمثلة التالية الكيفية التي يمكنك بها استخدام معلومات التتبع:</span><span class="sxs-lookup"><span data-stu-id="9de02-106">The following examples show how you can use the tracing information:</span></span>

-   <span data-ttu-id="9de02-107">عرض العلاقات بين الإجراءات في الأوامر المخططة لتحسين حجوزات المخزون وسلسلة التوريد.</span><span class="sxs-lookup"><span data-stu-id="9de02-107">View relations between the actions on planned orders to optimize the supply chain and inventory reservations.</span></span>
-   <span data-ttu-id="9de02-108">عرض العلاقات للأوامر التي تمت الموافقة عليها مسبقاً.</span><span class="sxs-lookup"><span data-stu-id="9de02-108">View relations to orders that are already approved.</span></span> <span data-ttu-id="9de02-109">يمكنك التركيز تلقائياً على تأكيد المتطلبات المشتقة ثم تحديد أولويات الأوامر بدقة أكبر.</span><span class="sxs-lookup"><span data-stu-id="9de02-109">You can focus on automatically firming derived requirements and then prioritize orders more accurately.</span></span>
-   <span data-ttu-id="9de02-110">محاكاة نتائج التخطيط لتحديد ما إذا كانت محددات التخطيط مثلى.</span><span class="sxs-lookup"><span data-stu-id="9de02-110">Simulate planning results to determine whether the planning parameters are optimal.</span></span>
-   <span data-ttu-id="9de02-111">تحديد الكيفية التي يتم بها تحديد المعلومات مثل تواريخ الإنتاج والكميات وأولويات لأمر.</span><span class="sxs-lookup"><span data-stu-id="9de02-111">Identify how information such as production dates, quantities, and priorities for an order were determined.</span></span>

<span data-ttu-id="9de02-112">يمكنك عرض تفاصيل حول العمليات الآجلة والإجراءات الخاصة بأمر محدد.</span><span class="sxs-lookup"><span data-stu-id="9de02-112">You can view details about futures and actions for a selected order.</span></span> <span data-ttu-id="9de02-113">وفي صفحة **تحديد إجمالي المكونات المطلوبة‬**، تتوفر معلومات التتبع في علامة التبويب **شرح** في الجزء العلوي.</span><span class="sxs-lookup"><span data-stu-id="9de02-113">On the **Explosion** page, tracing information is available on the **Explanation** tab in the upper pane.</span></span> <span data-ttu-id="9de02-114">يتم التتبع عند القيام بتحديد إجمالي المكونات المطلوبة لأمر.</span><span class="sxs-lookup"><span data-stu-id="9de02-114">Tracing occurs when you explode an order.</span></span> <span data-ttu-id="9de02-115">ولبدء التتبع للأمر، انقر فوق **تحديث**، ثم قم بتحديد خانة الاختيار **تمكين التتبع**.</span><span class="sxs-lookup"><span data-stu-id="9de02-115">To start tracing for the order, click **Update**, and then select the **Enable trace** check box.</span></span> <span data-ttu-id="9de02-116">ويمكنك استخدام حقل **البحث عن نص** للبحث عن سجل المعلومات الخاصة.</span><span class="sxs-lookup"><span data-stu-id="9de02-116">You can use the **Find text** field to search the log for specific information.</span></span> <span data-ttu-id="9de02-117">يتم تمييز نتائج البحث في الشجرة.</span><span class="sxs-lookup"><span data-stu-id="9de02-117">Search results are highlighted in the tree.</span></span>

<a name="additional-resources"></a><span data-ttu-id="9de02-118">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="9de02-118">Additional resources</span></span>
--------

[<span data-ttu-id="9de02-119">نظرة عامة على الخطط الرئيسية</span><span class="sxs-lookup"><span data-stu-id="9de02-119">Master plans overview</span></span>](master-plans.md)



