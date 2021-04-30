---
title: تعديل التنبؤ بالطلب يدوياً
description: يوضح هذا الموضوع كيفية تعديل التنبؤ لصنف ما.
author: ChristianRytt
ms.date: 08/12/2019
ms.topic: business-process
ms.search.form: EcoResProductDetailsExtended, ForecastSales
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5da1d5b1fbd91964e695a704681b1c9ee513a2f1
ms.sourcegitcommit: 4016c223a985c46e33f9941bf91ba5e1583e1cfd
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/13/2021
ms.locfileid: "5889014"
---
# <a name="modify-a-demand-forecast-manually"></a><span data-ttu-id="279e8-103">تعديل التنبؤ بالطلب يدوياً</span><span class="sxs-lookup"><span data-stu-id="279e8-103">Modify a demand forecast manually</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="279e8-104">يوضح هذا الإجراء كيفية تعديل التنبؤ لصنف ما.</span><span class="sxs-lookup"><span data-stu-id="279e8-104">This procedure shows how to modify the forecast for an item.</span></span> <span data-ttu-id="279e8-105">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي USMF.</span><span class="sxs-lookup"><span data-stu-id="279e8-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="279e8-106">هذا الإجراء مخصص لمخطط الإنتاج‬.</span><span class="sxs-lookup"><span data-stu-id="279e8-106">This procedure is intended for the production planner.</span></span>

## <a name="modify-the-forecast-for-a-selected-item"></a><span data-ttu-id="279e8-107">تعديل التنبؤ لصنف محدد</span><span class="sxs-lookup"><span data-stu-id="279e8-107">Modify the forecast for a selected item</span></span>

<span data-ttu-id="279e8-108">لتعديل التنبؤ لصنف محدد</span><span class="sxs-lookup"><span data-stu-id="279e8-108">To modify the forecast for a selected item:</span></span>

1. <span data-ttu-id="279e8-109">انتقل إلى **الوحدات النمطية \> إدارة معلومات المنتج \> المنتجات \> المنتجات الصادرة**.</span><span class="sxs-lookup"><span data-stu-id="279e8-109">Go to **Modules \> Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="279e8-110">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="279e8-110">In the list, find and select the desired record.</span></span> <span data-ttu-id="279e8-111">حدد الصنف الذي تريد تعديل التنبؤ الخاص به.</span><span class="sxs-lookup"><span data-stu-id="279e8-111">Select the item for which you want to modify the forecast.</span></span>
1. <span data-ttu-id="279e8-112">في جزء الإجراءات، افتح علامة التبويب **الخطة**، ثم حدد **التنبؤ بالطلب**.</span><span class="sxs-lookup"><span data-stu-id="279e8-112">On the Action Pane, open the **Plan** tab and select **Demand forecast**.</span></span>
1. <span data-ttu-id="279e8-113">في القائمة، حدد صفًا.</span><span class="sxs-lookup"><span data-stu-id="279e8-113">In the list, select a row.</span></span> <span data-ttu-id="279e8-114">إذا لم يكن هناك أي بنود تنبؤ، فيمكنك إنشاء بند جديد بالنقر فوق **جديد** في جزء الإجراءات.</span><span class="sxs-lookup"><span data-stu-id="279e8-114">If there are no forecast lines, create a new line by selecting **New** on the Action Pane.</span></span>  
1. <span data-ttu-id="279e8-115">في الحقل **كمية المبيعات**، أدخل رقمًا موجبًا.</span><span class="sxs-lookup"><span data-stu-id="279e8-115">In the **Sales quantity** field, enter a positive number.</span></span> <span data-ttu-id="279e8-116">يمثل هذا الرقم الكمية المتوقعة للصنف.</span><span class="sxs-lookup"><span data-stu-id="279e8-116">This number represents the forecasted quantity for the item.</span></span> <span data-ttu-id="279e8-117">سيظهر خطأ إذا قمت بإدخال رقم سالب.</span><span class="sxs-lookup"><span data-stu-id="279e8-117">An error will be shown if you enter a negative number.</span></span>
1. <span data-ttu-id="279e8-118">قم بملء الحقول الأخرى، حسب الحاجة.</span><span class="sxs-lookup"><span data-stu-id="279e8-118">Fill out the other fields as needed.</span></span>
1. <span data-ttu-id="279e8-119">في جزء الإجراءات، حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="279e8-119">Select **Save** on the Action Pane.</span></span>

## <a name="modify-the-forecast-for-one-or-more-items-microsoft-excel"></a><span data-ttu-id="279e8-120">تعديل التنبؤ لصنف واحد أو أكثر في Microsoft Excel</span><span class="sxs-lookup"><span data-stu-id="279e8-120">Modify the forecast for one or more items Microsoft Excel</span></span>

<span data-ttu-id="279e8-121">لتعديل التنبؤ لصنف واحد أو أكثر في Microsoft Excel:</span><span class="sxs-lookup"><span data-stu-id="279e8-121">To modify the forecast for one or more items Microsoft Excel:</span></span>

1. <span data-ttu-id="279e8-122">قم بأحد الإجراءين التاليين:</span><span class="sxs-lookup"><span data-stu-id="279e8-122">Do one of the following:</span></span>
    - <span data-ttu-id="279e8-123">افتح صفحة **التنبؤ بالطلب** لأي صنف كما ورد في القسم السابق.</span><span class="sxs-lookup"><span data-stu-id="279e8-123">Open the **Demand forecast** page for any item (it doesn't matter which one) as described in the previous section.</span></span>
    - <span data-ttu-id="279e8-124">انتقل إلى **التخطيط الرئيسي \> تنبؤ‬ \> إدخال التنبؤ اليدوي \> بنود التنبؤ بالطلب**.</span><span class="sxs-lookup"><span data-stu-id="279e8-124">Go to **Master planning \> Forecasting \> Manual forecast entry \> Demand forecast lines**.</span></span>
1. <span data-ttu-id="279e8-125">في جزء الإجراءات، حدد **فتح في Microsoft Office \> إدخالات التنبؤ بالطلب**.</span><span class="sxs-lookup"><span data-stu-id="279e8-125">On the Action Pane, select **Open in Microsoft Office \> Demand forecast entries**.</span></span>
1. <span data-ttu-id="279e8-126">حدد موقع تنزيل، ثم احفظه، ثم افتح الملف الذي تم تنزيله في Excel.</span><span class="sxs-lookup"><span data-stu-id="279e8-126">Select a download location, save, and then open the downloaded file in Excel.</span></span>
1. <span data-ttu-id="279e8-127">إذا شاهدت تحذيرًا، فاختر **تمكين التحرير**.</span><span class="sxs-lookup"><span data-stu-id="279e8-127">If you see a warning, choose to **Enable editing**.</span></span>
1. <span data-ttu-id="279e8-128">في Excel، سجل دخولك إلى Supply Chain Management باستخدام جزء المهام في Microsoft Dynamics.</span><span class="sxs-lookup"><span data-stu-id="279e8-128">In Excel, sign in to Supply Chain Management using the Microsoft Dynamics task pane.</span></span> <span data-ttu-id="279e8-129">يجب عليك تسجيل الدخول مع تمكين الخيار **الاستمرار في تسجيل الدخول** ويجب عليك الوثوق بتطبيق اتصال البيانات.</span><span class="sxs-lookup"><span data-stu-id="279e8-129">You must sign in with the **Keep me signed in** option enabled and you must trust the data connection app.</span></span>
1. <span data-ttu-id="279e8-130">يعرض جدول بيانات Excel الآن كافة بنود التنبؤ بالطلب الحالي لشركتك.</span><span class="sxs-lookup"><span data-stu-id="279e8-130">The Excel spreadsheet now shows all the current demand forecast lines for your company.</span></span>  <span data-ttu-id="279e8-131">يمكنك إضافة بنود التنبؤ بالطلب وحذفها وتحريرها وفق الحاجة.</span><span class="sxs-lookup"><span data-stu-id="279e8-131">Add, delete, and edit demand forecast lines as needed.</span></span>
1. <span data-ttu-id="279e8-132">حدد **نشر** على جزء المهام في Microsoft Dynamics لتحميل تغييراتك من جديد إلى Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="279e8-132">Select **Publish** on the Microsoft Dynamics task pane to upload your changes back to Supply Chain Management.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
