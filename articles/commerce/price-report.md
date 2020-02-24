---
title: تقارير أسعار البيع بالتجزئة
description: يوفر هذا الموضوع نظرة عامة حول ميزة تقرير الأسعار الذي يمكن استخدامه لعرض التغييرات المقبلة في الأسعار للمنتجات المصنفة.
author: shajain
manager: AnnBe
ms.date: 03/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 16181
ms.assetid: b1b57734-1406-4ed6-8e28-21c705ee17e2
ms.search.region: global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2019-01-18
ms.dyn365.ops.version: AX 10.0.0
ms.openlocfilehash: 91c0a96abdd7df9e85e63ca6b1b47a57f3f401eb
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/01/2020
ms.locfileid: "3021526"
---
# <a name="retail-price-reports"></a><span data-ttu-id="8bdae-103">تقارير أسعار البيع بالتجزئة</span><span class="sxs-lookup"><span data-stu-id="8bdae-103">Retail price reports</span></span>

[!include [banner](includes/banner.md)]


<span data-ttu-id="8bdae-104">يعمل بائعو التجزئة في الكثير من الأحيان الأسعار على تغيير أسعار المنتجات بهدف تقديم أسعار تنافسية لعملائهم.</span><span class="sxs-lookup"><span data-stu-id="8bdae-104">In order to provide competitive prices to their customers, retailers often change prices of products.</span></span> <span data-ttu-id="8bdae-105">يرغب مدراء المتاجر في الحصول على إمكانية الوصول بسهولة إلى التغييرات في الأسعار، الحديثة منها أو القادمة، لكي يتمكنوا من التخطيط للموارد المطلوبة لتحديث ملصقات الأسعار المعروضة على أرفف المتجر.</span><span class="sxs-lookup"><span data-stu-id="8bdae-105">Store managers want the ability to easily access recent or upcoming price changes so that they can plan for the required resources to update the price labels displayed on the store shelves.</span></span> <span data-ttu-id="8bdae-106">مع الإصدار 10.0 من Retail، بإمكان مدير المتجر أن يفتح تقرير **الأسعار** عن طريق الانتقال إلى **جميع المتاجر \> المتجر \> تقرير الأسعار** وعرض الأسعار المحدّثة للمنتجات المرتبطة بالمتجر.</span><span class="sxs-lookup"><span data-stu-id="8bdae-106">With release 10.0 of Retail, a store manager can open the **Price** report by navigating to **All stores \> Store \> Price report** and viewing the updated prices for the products associated to the store.</span></span> 

<span data-ttu-id="8bdae-107">لتمكين تقرير الأسعار يجب تشغيل المعلمة، **تمكين تقرير الأسعار لمتجر**.</span><span class="sxs-lookup"><span data-stu-id="8bdae-107">To enable the price report, the **Enable price report for store** parameter must be turned on.</span></span> <span data-ttu-id="8bdae-108">توجد هذه المعلمة على علامة التبويب **معلمات Commerce\> الخصومات \> متنوعة‬**. يؤدي فتح صفحة **تقرير الأسعار** إلى عرض مربع حوار يتضمن تكوينات مختلفة.</span><span class="sxs-lookup"><span data-stu-id="8bdae-108">This parameter is located on the **Commerce parameters \> Discounts \> Miscellaneous** tab. Opening the **Price report** page displays a dialog box with various configurations.</span></span> <span data-ttu-id="8bdae-109">تم إدراج أدناه التكوينات المتوفرة.</span><span class="sxs-lookup"><span data-stu-id="8bdae-109">The available configurations are listed below.</span></span>

| <span data-ttu-id="8bdae-110">التكوين</span><span class="sxs-lookup"><span data-stu-id="8bdae-110">Configuration</span></span> | <span data-ttu-id="8bdae-111">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="8bdae-111">Description</span></span> |
|---|---|
| <span data-ttu-id="8bdae-112">تاريخ "من" / تاريخ "إلى"</span><span class="sxs-lookup"><span data-stu-id="8bdae-112">From date / To date</span></span>| <span data-ttu-id="8bdae-113">نطاق التاريخ الذي يجب إنشاء تقرير الأسعار له.</span><span class="sxs-lookup"><span data-stu-id="8bdae-113">The date range for which the price report should be generated.</span></span> <span data-ttu-id="8bdae-114">المدة محددة بسبعة (7) أيام في الوقت الحالي.</span><span class="sxs-lookup"><span data-stu-id="8bdae-114">The duration is currently limited to 7 days.</span></span> |
| <span data-ttu-id="8bdae-115">التدفقات</span><span class="sxs-lookup"><span data-stu-id="8bdae-115">Channel</span></span>| <span data-ttu-id="8bdae-116">المتجر الذي يجب إنشاء تقرير الأسعار له.</span><span class="sxs-lookup"><span data-stu-id="8bdae-116">The store for which the price report should be generated.</span></span> |
| <span data-ttu-id="8bdae-117">عرض منتجات مع المخزون المتوفر</span><span class="sxs-lookup"><span data-stu-id="8bdae-117">Display products with available inventory</span></span>| <span data-ttu-id="8bdae-118">يؤدي تعيين هذا الخيار إلى **نعم** إلى عرض أسعار فقط المنتجات التي لديها مخزون فعلي في المتجر.</span><span class="sxs-lookup"><span data-stu-id="8bdae-118">Setting this to **Yes** will show the prices for only those products which currently have physical inventory available in the store.</span></span> |
| <span data-ttu-id="8bdae-119">عرض أسعار للمتغيرات</span><span class="sxs-lookup"><span data-stu-id="8bdae-119">Display prices for variants</span></span> | <span data-ttu-id="8bdae-120">يؤدي تعيين هذا الخيار إلى **نعم** إلى عرض أسعار المتغيرات مع أصول المنتجات.</span><span class="sxs-lookup"><span data-stu-id="8bdae-120">Setting this to **Yes** will display the prices of the variants along with the product masters.</span></span> <span data-ttu-id="8bdae-121">يجب **تشغيل** هذا الخيار فقط عند وجود أسعار متغيرات معينة، لأن عدد الصفوف يصبح كبيرًا جدًا.</span><span class="sxs-lookup"><span data-stu-id="8bdae-121">This should only be turned **On** if you have variant-specific prices, because the number of rows grows very large.</span></span> <span data-ttu-id="8bdae-122">في الإصدارات المستقبلية، سنعمل على تمكين الأسعار المستندة إلى الأبعاد لتمكين مدير المتجر من اختيار الأبعاد التي يجب عرض الأسعار لها.</span><span class="sxs-lookup"><span data-stu-id="8bdae-122">In future releases, we will enable the dimensions-based prices so that the store manager can choose the dimensions for which the prices should be displayed.</span></span> |
| <span data-ttu-id="8bdae-123">عرض منتجات مع تغييرات الأسعار</span><span class="sxs-lookup"><span data-stu-id="8bdae-123">Display products with price changes</span></span> | <span data-ttu-id="8bdae-124">يؤدي تعيين هذا الخيار إلى **نعم** إلى عرض الأسعار فقط للتواريخ التي تم فيها تغيير السعر.</span><span class="sxs-lookup"><span data-stu-id="8bdae-124">Setting this to **Yes** will display the prices for only those dates on which the price has been changed.</span></span> <span data-ttu-id="8bdae-125">سيكون السعر *قبل يوم واحد* من **التاريخ "من"** المحدد معروضًا بشكل دائم، لتمكين مدير المتجر من التعرف بسهولة على المنتجات التي لم تتغير أسعارها خلال المدة المحددة، ولتمكينه أيضًا من عرض السعر الحالي.</span><span class="sxs-lookup"><span data-stu-id="8bdae-125">The price for *one day before* the selected **From date** will always be displayed, so that the store manager can easily identity the products which have not changed prices for the entire selected duration, and can also view the current price.</span></span> |

<span data-ttu-id="8bdae-126">بعد إنشاء التقرير، يمكن تنزيل ملف Excel لإجراء أي عمليات تصفية إضافية مطلوبة.</span><span class="sxs-lookup"><span data-stu-id="8bdae-126">After the report is generated, the Excel file can be downloaded for any additional filtering needs.</span></span> <span data-ttu-id="8bdae-127">يمكن استخدام تقرير الأسعار أيضًا للتحقق من الأسعار القديمة للمنتجات للتواريخ السابقة.</span><span class="sxs-lookup"><span data-stu-id="8bdae-127">The price report can also be used to check the historical prices of products for past dates.</span></span>
