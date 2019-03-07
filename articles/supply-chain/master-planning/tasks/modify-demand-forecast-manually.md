---
title: تعديل التنبؤ بالطلب يدوياً
description: يوضح هذا الإجراء كيفية تعديل التنبؤ لصنف ما.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, ForecastSales
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 063554c98b8a6261ebe69073f214a8e45850c623
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/29/2019
ms.locfileid: "323584"
---
# <a name="modify-a-demand-forecast-manually"></a><span data-ttu-id="cd824-103">تعديل التنبؤ بالطلب يدوياً</span><span class="sxs-lookup"><span data-stu-id="cd824-103">Modify a demand forecast manually</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="cd824-104">يوضح هذا الإجراء كيفية تعديل التنبؤ لصنف ما.</span><span class="sxs-lookup"><span data-stu-id="cd824-104">This procedure shows how to modify the forecast for an item.</span></span> <span data-ttu-id="cd824-105">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي USMF.</span><span class="sxs-lookup"><span data-stu-id="cd824-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="cd824-106">هذا التسجيل مخصص لمخطط الإنتاج‬.</span><span class="sxs-lookup"><span data-stu-id="cd824-106">This recording is intended for the production planner.</span></span> 


## <a name="modify-the-forecast-for-an-item"></a><span data-ttu-id="cd824-107">تعديل التنبؤ لصنف</span><span class="sxs-lookup"><span data-stu-id="cd824-107">Modify the forecast for an item</span></span>
1. <span data-ttu-id="cd824-108">انتقل إلى إدارة معلومات المنتج > المنتجات > المنتجات الصادرة.</span><span class="sxs-lookup"><span data-stu-id="cd824-108">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="cd824-109">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="cd824-109">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="cd824-110">حدد الصنف الذي تريد تعديل التنبؤ الخاص به.</span><span class="sxs-lookup"><span data-stu-id="cd824-110">Select the item for which you want to modify the forecast.</span></span> <span data-ttu-id="cd824-111">على سبيل المثال، يمكنك تحديد الصنف D0001.</span><span class="sxs-lookup"><span data-stu-id="cd824-111">For example, you can select item D0001.</span></span>  
3. <span data-ttu-id="cd824-112">في جزء "الإجراءات"، انقر فوق "خطة".</span><span class="sxs-lookup"><span data-stu-id="cd824-112">On the Action Pane, click Plan.</span></span>
4. <span data-ttu-id="cd824-113">انقر فوق "التنبؤ بالطلب".</span><span class="sxs-lookup"><span data-stu-id="cd824-113">Click Demand forecast.</span></span>
5. <span data-ttu-id="cd824-114">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="cd824-114">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="cd824-115">إذا كانت هناك أي بنود تنبؤ، فيتم إنشاء بند جديد عن طريق</span><span class="sxs-lookup"><span data-stu-id="cd824-115">If there are no forecast lines, create a new line by  .</span></span> <span data-ttu-id="cd824-116">النقر فوق "جديد" على شريط التطبيق.</span><span class="sxs-lookup"><span data-stu-id="cd824-116">clicking New on the app bar.</span></span>  
6. <span data-ttu-id="cd824-117">في الحقل "كمية المبيعات"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="cd824-117">In the Sales quantity field, enter a number.</span></span>
    * <span data-ttu-id="cd824-118">يمثل هذا الرقم الكمية المتوقعة للصنف.</span><span class="sxs-lookup"><span data-stu-id="cd824-118">This number represents the forecasted quantity for the item.</span></span>  
7. <span data-ttu-id="cd824-119">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="cd824-119">Click Save.</span></span>

## <a name="modify-the-forecast-in-excel"></a><span data-ttu-id="cd824-120">تعديل التنبؤ في Excel</span><span class="sxs-lookup"><span data-stu-id="cd824-120">Modify the forecast in Excel</span></span>
1. <span data-ttu-id="cd824-121">انقر فوق فتح في Microsoft Office.</span><span class="sxs-lookup"><span data-stu-id="cd824-121">Click Open in Microsoft Office.</span></span>
2. <span data-ttu-id="cd824-122">انقر فوق "تحرير التنبؤ بالطلب" في Excel.</span><span class="sxs-lookup"><span data-stu-id="cd824-122">Click Edit Demand forecast in Excel.</span></span>
    * <span data-ttu-id="cd824-123">في Excel، يمكنك إضافة بنود التنبؤ بالطلب وحذفها وتحريرها.</span><span class="sxs-lookup"><span data-stu-id="cd824-123">In Excel, you can add, delete and edit demand forecast lines.</span></span> <span data-ttu-id="cd824-124">إذا لم تتمكن من رؤية البيانات في Excel، فستحتاج إلى تسجيل الدخول إلى Microsoft Dynamics 365 for Finance and Operations, Enterprise edition مع تمكين خيار "الاستمرار في تسجيل الدخول" وتحتاج إلى الثقة بتطبيق اتصال بيانات.</span><span class="sxs-lookup"><span data-stu-id="cd824-124">If you are not able to see the data in Excel, you need to sign in to Microsoft Dynamics 365 for Finance and Operations, Enterprise edition with the "Keep me signed in" option enabled and you need to trust the data connection app.</span></span>  

