---
title: تعديل التنبؤ بالطلب يدوياً
description: يوضح هذا الإجراء كيفية تعديل التنبؤ لصنف ما.
author: ShylaThompson
manager: AnnBe
ms.date: 08/12/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, ForecastSales
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 58846f896d60610d0e90f8d04fda3101def53511
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/18/2020
ms.locfileid: "3148091"
---
# <a name="modify-a-demand-forecast-manually"></a><span data-ttu-id="26e12-103">تعديل التنبؤ بالطلب يدوياً</span><span class="sxs-lookup"><span data-stu-id="26e12-103">Modify a demand forecast manually</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="26e12-104">يوضح هذا الإجراء كيفية تعديل التنبؤ لصنف ما.</span><span class="sxs-lookup"><span data-stu-id="26e12-104">This procedure shows how to modify the forecast for an item.</span></span> <span data-ttu-id="26e12-105">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي USMF.</span><span class="sxs-lookup"><span data-stu-id="26e12-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="26e12-106">هذا التسجيل مخصص لمخطط الإنتاج‬.</span><span class="sxs-lookup"><span data-stu-id="26e12-106">This recording is intended for the production planner.</span></span> 


## <a name="modify-the-forecast-for-an-item"></a><span data-ttu-id="26e12-107">تعديل التنبؤ لصنف</span><span class="sxs-lookup"><span data-stu-id="26e12-107">Modify the forecast for an item</span></span>
1. <span data-ttu-id="26e12-108">‏‫في **جزء التنقل**، انتقل إلى **الوحدات النمطية > إدارة معلومات المنتج > المنتجات > المنتجات الصادرة**‬‏‎.</span><span class="sxs-lookup"><span data-stu-id="26e12-108">In the **Navigation pane**, go to **Modules > Product information management > Products > Released products**.</span></span>
2. <span data-ttu-id="26e12-109">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="26e12-109">In the list, find and select the desired record.</span></span> <span data-ttu-id="26e12-110">حدد الصنف الذي تريد تعديل التنبؤ الخاص به.</span><span class="sxs-lookup"><span data-stu-id="26e12-110">Select the item for which you want to modify the forecast.</span></span> <span data-ttu-id="26e12-111">على سبيل المثال، يمكنك تحديد الصنف D0001.</span><span class="sxs-lookup"><span data-stu-id="26e12-111">For example, you can select item D0001.</span></span>  
3. <span data-ttu-id="26e12-112">في **جزء الإجراءات**، انقر فوق **الخطة**.</span><span class="sxs-lookup"><span data-stu-id="26e12-112">On the **Action Pane**, click **Plan**.</span></span>
4. <span data-ttu-id="26e12-113">انقر فوق **التنبؤ بالطلب**.</span><span class="sxs-lookup"><span data-stu-id="26e12-113">Click **Demand forecast**.</span></span>
5. <span data-ttu-id="26e12-114">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="26e12-114">In the list, mark the selected row.</span></span> <span data-ttu-id="26e12-115">إذا لم يكن هناك أي بنود تنبؤ، فيمكنك إنشاء بند جديد بالنقر فوق "جديد" في شريط التطبيق.</span><span class="sxs-lookup"><span data-stu-id="26e12-115">If there are no forecast lines, create a new line by clicking New on the app bar.</span></span>  
6. <span data-ttu-id="26e12-116">في الحقل **كمية المبيعات**، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="26e12-116">In the **Sales quantity** field, enter a number.</span></span> <span data-ttu-id="26e12-117">يمثل هذا الرقم الكمية المتوقعة للصنف.</span><span class="sxs-lookup"><span data-stu-id="26e12-117">This number represents the forecasted quantity for the item.</span></span>  
7. <span data-ttu-id="26e12-118">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="26e12-118">Click Save.</span></span>

## <a name="modify-the-forecast-in-excel"></a><span data-ttu-id="26e12-119">تعديل التنبؤ في Excel</span><span class="sxs-lookup"><span data-stu-id="26e12-119">Modify the forecast in Excel</span></span>
1. <span data-ttu-id="26e12-120">انقر فوق **فتح** في Microsoft Office.</span><span class="sxs-lookup"><span data-stu-id="26e12-120">Click **Open** in Microsoft Office.</span></span>
2. <span data-ttu-id="26e12-121">انقر فوق **تحرير التنبؤ بالطلب** في Excel.</span><span class="sxs-lookup"><span data-stu-id="26e12-121">Click **Edit Demand forecast** in Excel.</span></span> <span data-ttu-id="26e12-122">في Excel، يمكنك إضافة بنود التنبؤ بالطلب وحذفها وتحريرها.</span><span class="sxs-lookup"><span data-stu-id="26e12-122">In Excel, you can add, delete and edit demand forecast lines.</span></span> <span data-ttu-id="26e12-123">إذا لم تتمكن من رؤية البيانات في Excel، فستحتاج إلى تسجيل الدخول مع تمكين خيار "الاستمرار في تسجيل الدخول" وتحتاج إلى الثقة بتطبيق اتصال بيانات.</span><span class="sxs-lookup"><span data-stu-id="26e12-123">If you are not able to see the data in Excel, you need to sign in with the "Keep me signed in" option enabled and you need to trust the data connection app.</span></span>  

