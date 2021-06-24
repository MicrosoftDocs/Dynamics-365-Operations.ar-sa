---
title: 'دليل: تعديل التنبؤ بالطلب يدويًا'
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
ms.openlocfilehash: 1e12ccf90b9971379e8931bd48d6243a855bb795
ms.sourcegitcommit: 15aacd0e109b05c7281407b5bba4e6cd99116c28
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/10/2021
ms.locfileid: "6224000"
---
# <a name="guide-modify-a-demand-forecast-manually"></a><span data-ttu-id="11af0-103">دليل: تعديل التنبؤ بالطلب يدويًا</span><span class="sxs-lookup"><span data-stu-id="11af0-103">Guide: Modify a demand forecast manually</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="11af0-104">يوضح هذا الإجراء كيفية تعديل التنبؤ لصنف ما.</span><span class="sxs-lookup"><span data-stu-id="11af0-104">This procedure shows how to modify the forecast for an item.</span></span> <span data-ttu-id="11af0-105">هذا الإجراء مخصص لمخطط الإنتاج‬.</span><span class="sxs-lookup"><span data-stu-id="11af0-105">This procedure is intended for the production planner.</span></span>

## <a name="modify-the-forecast-for-a-selected-item"></a><span data-ttu-id="11af0-106">تعديل التنبؤ لصنف محدد</span><span class="sxs-lookup"><span data-stu-id="11af0-106">Modify the forecast for a selected item</span></span>

<span data-ttu-id="11af0-107">لتعديل التنبؤ لصنف محدد</span><span class="sxs-lookup"><span data-stu-id="11af0-107">To modify the forecast for a selected item:</span></span>

1. <span data-ttu-id="11af0-108">انتقل إلى **الوحدات النمطية \> إدارة معلومات المنتج \> المنتجات \> المنتجات الصادرة**.</span><span class="sxs-lookup"><span data-stu-id="11af0-108">Go to **Modules \> Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="11af0-109">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="11af0-109">In the list, find and select the desired record.</span></span> <span data-ttu-id="11af0-110">حدد الصنف الذي تريد تعديل التنبؤ الخاص به.</span><span class="sxs-lookup"><span data-stu-id="11af0-110">Select the item for which you want to modify the forecast.</span></span>
1. <span data-ttu-id="11af0-111">في جزء الإجراءات، افتح علامة التبويب **الخطة**، ثم حدد **التنبؤ بالطلب**.</span><span class="sxs-lookup"><span data-stu-id="11af0-111">On the Action Pane, open the **Plan** tab and select **Demand forecast**.</span></span>
1. <span data-ttu-id="11af0-112">في القائمة، حدد صفًا.</span><span class="sxs-lookup"><span data-stu-id="11af0-112">In the list, select a row.</span></span> <span data-ttu-id="11af0-113">إذا لم يكن هناك أي بنود تنبؤ، فيمكنك إنشاء بند جديد بالنقر فوق **جديد** في جزء الإجراءات.</span><span class="sxs-lookup"><span data-stu-id="11af0-113">If there are no forecast lines, create a new line by selecting **New** on the Action Pane.</span></span>  
1. <span data-ttu-id="11af0-114">في الحقل **كمية المبيعات**، أدخل رقمًا موجبًا.</span><span class="sxs-lookup"><span data-stu-id="11af0-114">In the **Sales quantity** field, enter a positive number.</span></span> <span data-ttu-id="11af0-115">يمثل هذا الرقم الكمية المتوقعة للصنف.</span><span class="sxs-lookup"><span data-stu-id="11af0-115">This number represents the forecasted quantity for the item.</span></span> <span data-ttu-id="11af0-116">سيظهر خطأ إذا قمت بإدخال رقم سالب.</span><span class="sxs-lookup"><span data-stu-id="11af0-116">An error will be shown if you enter a negative number.</span></span>
1. <span data-ttu-id="11af0-117">قم بملء الحقول الأخرى، حسب الحاجة.</span><span class="sxs-lookup"><span data-stu-id="11af0-117">Fill out the other fields as needed.</span></span>
1. <span data-ttu-id="11af0-118">في جزء الإجراءات، حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="11af0-118">Select **Save** on the Action Pane.</span></span>

## <a name="modify-the-forecast-for-one-or-more-items-with-microsoft-excel"></a><span data-ttu-id="11af0-119">تعديل التنبؤ لصنف واحد أو أكثر باستخدام Microsoft Excel:</span><span class="sxs-lookup"><span data-stu-id="11af0-119">Modify the forecast for one or more items with Microsoft Excel</span></span>

<span data-ttu-id="11af0-120">لتعديل التنبؤ لصنف واحد أو أكثر باستخدام Microsoft Excel:</span><span class="sxs-lookup"><span data-stu-id="11af0-120">To modify the forecast for one or more items with Microsoft Excel:</span></span>

1. <span data-ttu-id="11af0-121">قم بأحد الإجراءين التاليين:</span><span class="sxs-lookup"><span data-stu-id="11af0-121">Do one of the following:</span></span>
    - <span data-ttu-id="11af0-122">افتح صفحة **التنبؤ بالطلب** لأي صنف كما ورد في القسم السابق.</span><span class="sxs-lookup"><span data-stu-id="11af0-122">Open the **Demand forecast** page for any item (it doesn't matter which one) as described in the previous section.</span></span>
    - <span data-ttu-id="11af0-123">انتقل إلى **التخطيط الرئيسي \> تنبؤ‬ \> إدخال التنبؤ اليدوي \> بنود التنبؤ بالطلب**.</span><span class="sxs-lookup"><span data-stu-id="11af0-123">Go to **Master planning \> Forecasting \> Manual forecast entry \> Demand forecast lines**.</span></span>
1. <span data-ttu-id="11af0-124">في جزء الإجراءات، حدد **فتح في Microsoft Office \> إدخالات التنبؤ بالطلب**.</span><span class="sxs-lookup"><span data-stu-id="11af0-124">On the Action Pane, select **Open in Microsoft Office \> Demand forecast entries**.</span></span>
1. <span data-ttu-id="11af0-125">حدد موقع تنزيل، ثم احفظه، ثم افتح الملف الذي تم تنزيله في Excel.</span><span class="sxs-lookup"><span data-stu-id="11af0-125">Select a download location, save, and then open the downloaded file in Excel.</span></span>
1. <span data-ttu-id="11af0-126">إذا شاهدت تحذيرًا، فاختر **تمكين التحرير**.</span><span class="sxs-lookup"><span data-stu-id="11af0-126">If you see a warning, choose to **Enable editing**.</span></span>
1. <span data-ttu-id="11af0-127">في Excel، سجل دخولك إلى Supply Chain Management باستخدام جزء المهام في Microsoft Dynamics.</span><span class="sxs-lookup"><span data-stu-id="11af0-127">In Excel, sign in to Supply Chain Management using the Microsoft Dynamics task pane.</span></span> <span data-ttu-id="11af0-128">يجب عليك تسجيل الدخول مع تمكين الخيار **الاستمرار في تسجيل الدخول** ويجب عليك الوثوق بتطبيق اتصال البيانات.</span><span class="sxs-lookup"><span data-stu-id="11af0-128">You must sign in with the **Keep me signed in** option enabled and you must trust the data connection app.</span></span>
1. <span data-ttu-id="11af0-129">يعرض جدول بيانات Excel الآن كافة بنود التنبؤ بالطلب الحالي لشركتك.</span><span class="sxs-lookup"><span data-stu-id="11af0-129">The Excel spreadsheet now shows all the current demand forecast lines for your company.</span></span>  <span data-ttu-id="11af0-130">يمكنك إضافة بنود التنبؤ بالطلب وحذفها وتحريرها وفق الحاجة.</span><span class="sxs-lookup"><span data-stu-id="11af0-130">Add, delete, and edit demand forecast lines as needed.</span></span>
1. <span data-ttu-id="11af0-131">حدد **نشر** على جزء المهام في Microsoft Dynamics لتحميل تغييراتك من جديد إلى Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="11af0-131">Select **Publish** on the Microsoft Dynamics task pane to upload your changes back to Supply Chain Management.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
