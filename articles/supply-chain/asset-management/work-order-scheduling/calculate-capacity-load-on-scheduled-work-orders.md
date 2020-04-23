---
title: حساب القدرة الإنتاجية على أوامر العمل المجدولة
description: يوضح هذا الموضوع كيفية حساب القدرة الإنتاجية على أوامر العمل المجدولة في إدارة الأصول.
author: josaw1
manager: tfehr
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: b817909ac0950b773cba775be2502b5796c6d8d6
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/02/2020
ms.locfileid: "3215345"
---
# <a name="calculate-capacity-load-on-scheduled-work-orders"></a><span data-ttu-id="fb01e-103">حساب القدرة الإنتاجية على أوامر العمل المجدولة</span><span class="sxs-lookup"><span data-stu-id="fb01e-103">Calculate capacity load on scheduled work orders</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="fb01e-104">يمكنك حساب القدرة الإنتاجية على أوامر العمل المجدولة للحصول على نظرة عامة حول حمل العمل على الموارد لفترة محددة.</span><span class="sxs-lookup"><span data-stu-id="fb01e-104">You can calculate capacity load on scheduled work orders to get an overview of the work load on resources for a specific period.</span></span> <span data-ttu-id="fb01e-105">يمكن إجراء الحسابات للموارد التالية: عاملو الصيانة ومجموعات العاملين والأدوات والأصول.</span><span class="sxs-lookup"><span data-stu-id="fb01e-105">Calculations can be made for the following resources: Maintenance workers, worker groups, tools, and assets.</span></span>

1. <span data-ttu-id="fb01e-106">انقر فوق **إدارة الأصول** > **استعلامات** > **الجدول** > **القدرة الإنتاجية**.</span><span class="sxs-lookup"><span data-stu-id="fb01e-106">Click **Asset management** > **Inquiries** > **Schedule** > **Capacity load**.</span></span>

2. <span data-ttu-id="fb01e-107">في مربع الحوار **حساب‏‎ القدرة الإنتاجية** > الحقل **إظهار** ، حدد نوع الحمل الذي تريد حسابه: **القدرة**، **المحجوز** أو **المتبقي‬**.</span><span class="sxs-lookup"><span data-stu-id="fb01e-107">In the **Calculate capacity load** dialog > **Show** field, select which load type you want to calculate: **Capacity**, **Reserved**, or **Remainder**.</span></span>

3. <span data-ttu-id="fb01e-108">حدد **نعم** على زر التبديل **تخطي الصفر** إذا لم ترغب في إظهار النتائج التي تحتوي على صفر.</span><span class="sxs-lookup"><span data-stu-id="fb01e-108">Select **Yes** on the **Skip zero** toggle button if you do not want to show results containing zero.</span></span>

4. <span data-ttu-id="fb01e-109">حدد أنواع الموارد التي ترغب في حساب القدرة الإنتاجية لها من خلال تحديد **نعم** على أزرار التبديل الملائمة: **العامل**، و **مجموعة عاملي الصيانة**، و **الأداة**، و **الأصل**.</span><span class="sxs-lookup"><span data-stu-id="fb01e-109">Select the resource types for which you want to calculate capacity load by selecting **Yes** on the relevant toggle buttons: **Worker**, **Maintenance worker group**, **Tool**, and **Asset**.</span></span>

5. <span data-ttu-id="fb01e-110">حدد تاريخ بدء الحساب في الحقل **من تاريخ**.</span><span class="sxs-lookup"><span data-stu-id="fb01e-110">Select the start date for the calculation in the **From date** field.</span></span>

6. <span data-ttu-id="fb01e-111">في الحقل **نوع الفاصل الزمني** ، حدد الفاصل الزمني للحساب: **يوم**، أو **أسبوع**، أو **شهر**، أو **ربع السنة**.</span><span class="sxs-lookup"><span data-stu-id="fb01e-111">In the **Interval type** field, select the interval for the calculation: **Day**, **Week**, **Month**, or **Quarter**.</span></span>

7. <span data-ttu-id="fb01e-112">في الحقل **تكرار الفترة‬**، أدخل عدد الفواصل الزمنية التي تريد حسابها.</span><span class="sxs-lookup"><span data-stu-id="fb01e-112">In the **Period frequency** field, insert the number of intervals you want to calculate.</span></span> <span data-ttu-id="fb01e-113">على سبيل المثال، إذا حددت **يوم** كنوع فاصل زمني، وأدرجت الرقم "5" في هذا الحقل، سيتم إجراء حساب خمسة أيام من تاريخ البدء.</span><span class="sxs-lookup"><span data-stu-id="fb01e-113">For example, if you have selected **Day** as the interval type, and you enter the number "5" in this field, a calculation of five days from the start date will be made.</span></span>

8. <span data-ttu-id="fb01e-114">انقر فوق **موافق** لبدء الحساب.</span><span class="sxs-lookup"><span data-stu-id="fb01e-114">Click **OK** to start the calculation.</span></span>

<span data-ttu-id="fb01e-115">يظهر الشكل أدناه نتيجة الحساب الذي يغطي ثلاثة أسابيع لنوع حمل العمل **محجوز**.</span><span class="sxs-lookup"><span data-stu-id="fb01e-115">The figure below shows the result of a calculation covering three weeks for the load type **Reserved**.</span></span>

![الشكل 1](media/08-work-order-scheduling.png)

[!NOTE]
<span data-ttu-id="fb01e-117">إذا قمت بتحديد أنواع حمل العمل **القدرة** أو **المتبقي** لعملية الحساب، فستظهر النتيجة نفسها إذا لم يتم إجراء أي حجوزات للموارد في الفترة المحددة.</span><span class="sxs-lookup"><span data-stu-id="fb01e-117">If you select the load types **Capacity** or **Remainder** for your calculation, the same result will be displayed if no reservations have been made for the resources in the selected period.</span></span>

<span data-ttu-id="fb01e-118">للحصول على معلومات حول كيفيه حساب القدرة الإنتاجية على بنود جدول الصيانة وليس على أوامر العمل المجدولة، راجع [حساب القدرة الإنتاجية](../capacity-planning/calculate-capacity-load.md).</span><span class="sxs-lookup"><span data-stu-id="fb01e-118">For information about how to calculate capacity load on maintenance schedule lines and not scheduled work orders, refer to [Calculate capacity load](../capacity-planning/calculate-capacity-load.md).</span></span>

