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
ms.openlocfilehash: 1ec1edb861619bae2ae3c211720b55e170b83ec9
ms.sourcegitcommit: cbcf344b3b552acca56c3e27606eac7f2f124afe
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/22/2019
ms.locfileid: "1916612"
---
# <a name="modify-a-demand-forecast-manually"></a><span data-ttu-id="c5a73-103">تعديل التنبؤ بالطلب يدوياً</span><span class="sxs-lookup"><span data-stu-id="c5a73-103">Modify a demand forecast manually</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c5a73-104">يوضح هذا الإجراء كيفية تعديل التنبؤ لصنف ما.</span><span class="sxs-lookup"><span data-stu-id="c5a73-104">This procedure shows how to modify the forecast for an item.</span></span> <span data-ttu-id="c5a73-105">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي USMF.</span><span class="sxs-lookup"><span data-stu-id="c5a73-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="c5a73-106">هذا التسجيل مخصص لمخطط الإنتاج‬.</span><span class="sxs-lookup"><span data-stu-id="c5a73-106">This recording is intended for the production planner.</span></span> 


## <a name="modify-the-forecast-for-an-item"></a><span data-ttu-id="c5a73-107">تعديل التنبؤ لصنف</span><span class="sxs-lookup"><span data-stu-id="c5a73-107">Modify the forecast for an item</span></span>
1. <span data-ttu-id="c5a73-108">‏‫في **جزء التنقل**، انتقل إلى **الوحدات النمطية > إدارة معلومات المنتج > المنتجات > المنتجات الصادرة**‬‏‎.</span><span class="sxs-lookup"><span data-stu-id="c5a73-108">In the **Navigation pane**, go to **Modules > Product information management > Products > Released products**.</span></span>
2. <span data-ttu-id="c5a73-109">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="c5a73-109">In the list, find and select the desired record.</span></span> <span data-ttu-id="c5a73-110">حدد الصنف الذي تريد تعديل التنبؤ الخاص به.</span><span class="sxs-lookup"><span data-stu-id="c5a73-110">Select the item for which you want to modify the forecast.</span></span> <span data-ttu-id="c5a73-111">على سبيل المثال، يمكنك تحديد الصنف D0001.</span><span class="sxs-lookup"><span data-stu-id="c5a73-111">For example, you can select item D0001.</span></span>  
3. <span data-ttu-id="c5a73-112">في **جزء الإجراءات**، انقر فوق **الخطة**.</span><span class="sxs-lookup"><span data-stu-id="c5a73-112">On the **Action Pane**, click **Plan**.</span></span>
4. <span data-ttu-id="c5a73-113">انقر فوق **التنبؤ بالطلب**.</span><span class="sxs-lookup"><span data-stu-id="c5a73-113">Click **Demand forecast**.</span></span>
5. <span data-ttu-id="c5a73-114">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="c5a73-114">In the list, mark the selected row.</span></span> <span data-ttu-id="c5a73-115">إذا لم يكن هناك أي بنود تنبؤ، فيمكنك إنشاء بند جديد بالنقر فوق "جديد" في شريط التطبيق.</span><span class="sxs-lookup"><span data-stu-id="c5a73-115">If there are no forecast lines, create a new line by clicking New on the app bar.</span></span>  
6. <span data-ttu-id="c5a73-116">في الحقل **كمية المبيعات**، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="c5a73-116">In the **Sales quantity** field, enter a number.</span></span> <span data-ttu-id="c5a73-117">يمثل هذا الرقم الكمية المتوقعة للصنف.</span><span class="sxs-lookup"><span data-stu-id="c5a73-117">This number represents the forecasted quantity for the item.</span></span>  
7. <span data-ttu-id="c5a73-118">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="c5a73-118">Click Save.</span></span>

## <a name="modify-the-forecast-in-excel"></a><span data-ttu-id="c5a73-119">تعديل التنبؤ في Excel</span><span class="sxs-lookup"><span data-stu-id="c5a73-119">Modify the forecast in Excel</span></span>
1. <span data-ttu-id="c5a73-120">انقر فوق **فتح** في Microsoft Office.</span><span class="sxs-lookup"><span data-stu-id="c5a73-120">Click **Open** in Microsoft Office.</span></span>
2. <span data-ttu-id="c5a73-121">انقر فوق **تحرير التنبؤ بالطلب** في Excel.</span><span class="sxs-lookup"><span data-stu-id="c5a73-121">Click **Edit Demand forecast** in Excel.</span></span> <span data-ttu-id="c5a73-122">في Excel، يمكنك إضافة بنود التنبؤ بالطلب وحذفها وتحريرها.</span><span class="sxs-lookup"><span data-stu-id="c5a73-122">In Excel, you can add, delete and edit demand forecast lines.</span></span> <span data-ttu-id="c5a73-123">إذا لم تتمكن من رؤية البيانات في Excel، فستحتاج إلى تسجيل الدخول إلى Microsoft Dynamics 365 for Finance and Operations, Enterprise edition مع تمكين خيار "الاستمرار في تسجيل الدخول" وتحتاج إلى الثقة بتطبيق اتصال بيانات.</span><span class="sxs-lookup"><span data-stu-id="c5a73-123">If you are not able to see the data in Excel, you need to sign in to Microsoft Dynamics 365 for Finance and Operations, Enterprise edition with the "Keep me signed in" option enabled and you need to trust the data connection app.</span></span>  

