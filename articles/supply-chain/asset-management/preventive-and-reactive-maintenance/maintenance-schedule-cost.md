---
title: تكلفة جدول الصيانة
description: يوضح هذا الموضوع تكلفة جدول الصيانة في إدارة الأصول.
author: josaw1
manager: tfehr
ms.date: 08/27/2019
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
ms.openlocfilehash: 91c5b2e70ee083bf2741e245f1ca840ab939ad3f
ms.sourcegitcommit: 8a2127c5af6cdbda30ccc1f9bef9bd4ab61e9e50
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/18/2020
ms.locfileid: "3382965"
---
# <a name="maintenance-schedule-cost"></a><span data-ttu-id="42a25-103">تكلفة جدول الصيانة</span><span class="sxs-lookup"><span data-stu-id="42a25-103">Maintenance schedule cost</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="42a25-104">في إدارة الأصول، يمكنك حساب تكاليف الموازنة في بنود جدول الصيانة.</span><span class="sxs-lookup"><span data-stu-id="42a25-104">In Asset Management, you can calculate budget costs on maintenance schedule lines.</span></span> <span data-ttu-id="42a25-105">ويكون ذلك مفيدًا إذا كنت ترغب في الحصول على نظرة عامة حول التكاليف المتوقعة، على سبيل المثال، التكاليف المتعلقة بمهام الصيانة الوقائية المخططة للسنة التالية.</span><span class="sxs-lookup"><span data-stu-id="42a25-105">This is useful if you want to get an overview of expected costs, for example, costs relating to planned preventive maintenance jobs for the next year.</span></span> <span data-ttu-id="42a25-106">تعتمد الحسابات على بنود جدول الصيانة الموجودة من نوع "خطط الصيانة" و "دورات الصيانة" و "طلبات الصيانة".</span><span class="sxs-lookup"><span data-stu-id="42a25-106">The calculations are based on existing maintenance schedule lines of type "Maintenance plans" and "Maintenance rounds" and "Maintenance requests".</span></span>

1. <span data-ttu-id="42a25-107">انقر فوق **إدارة الأصول** > **استعلامات** > **الأصول** > **تكلفة جدول الصيانة**.</span><span class="sxs-lookup"><span data-stu-id="42a25-107">Click **Asset management** > **Inquiries** > **Assets** > **Maintenance schedule cost**.</span></span>

2. <span data-ttu-id="42a25-108">في مربع الحوار **تكلفة جدول الصيانة**، يمكنك تحديد **مجموعة الأبعاد المالية‬** إذا كنت تريد الاطلاع على التكاليف المجمعة في الأبعاد المالية.</span><span class="sxs-lookup"><span data-stu-id="42a25-108">In the **Maintenance schedule cost** dialog, you can select a **Financial dimension set** if you want to see costs grouped in financial dimensions.</span></span>

>[!NOTE]
><span data-ttu-id="42a25-109">يتم إعداد مجموعات الأبعاد المالية في **دفتر الأستاذ العام** > **مخطط الحسابات** > **الأبعاد** > **مجموعات الأبعاد المالية**.</span><span class="sxs-lookup"><span data-stu-id="42a25-109">Financial dimension sets are set up in **General ledger** > **Chart of accounts** > **Dimensions** > **Financial dimension sets**.</span></span>

3. <span data-ttu-id="42a25-110">يمكنك استخدام حقل **المستوى** للإشارة إلى مستوى التفصيل الذي ترغب فيه في بنود جدول الصيانة فيما يتعلق بمواقع العمل.</span><span class="sxs-lookup"><span data-stu-id="42a25-110">You can use the **Level** field to indicate how detailed you want the maintenance schedule lines to be regarding functional locations.</span></span> <span data-ttu-id="42a25-111">على سبيل المثال، إذا قمت بإدخال الرقم "1" في الحقل، وكان لديك بنية موقع عمل متعدد المستويات، فستظهر جميع بنود جدول الصيانة لموقع عمل في المستوى الأعلى، وبالتالي فقد تُضاف الساعات إلى البند من مواقع عمل موجودة في مستوى أدنى.</span><span class="sxs-lookup"><span data-stu-id="42a25-111">For example, if you insert the number "1" in the field, and you have a multi-level functional location structure, all maintenance schedule lines for a functional location will be shown on the top level, and therefore the hours on a line may be added up from functional locations located at a lower level.</span></span> <span data-ttu-id="42a25-112">إذا قمت بإدخال الرقم "0" في حقل **المستوى**، فسترى نتيجة مفصلة تعرض جميع بنود جدول الصيانة على جميع مستويات مواقع العمل التي ترتبط بها.</span><span class="sxs-lookup"><span data-stu-id="42a25-112">If you insert the number "0" in the **Level** field, you will see a detailed result showing all maintenance schedule lines on all the functional location levels to which they are related.</span></span>

4. <span data-ttu-id="42a25-113">إذا أردت إجراء حساب لأصول معينة، فانقر فوق **عامل تصفية** على علامة التبويب السريعة **السجلات المطلوب تضمينها‬**، وحدد الأصول ذات الصلة.</span><span class="sxs-lookup"><span data-stu-id="42a25-113">If you want to make a calculation for specific assets, click **Filter** on the **Records to include** FastTab, and select the relevant assets.</span></span> <span data-ttu-id="42a25-114">وإذا لزم الأمر، فيمكنك أيضًا تحديد **تاريخ البدء المتوقع‬** لحساب التكلفة أو تحديد **حالة** مختلفة لحساب التكلفة</span><span class="sxs-lookup"><span data-stu-id="42a25-114">If required, you can also specify an **Expected start** date for the cost calculation or select a different **Status** for the cost calculation</span></span>

5. <span data-ttu-id="42a25-115">انقر فوق **موافق** لبدء حساب التكلفة.</span><span class="sxs-lookup"><span data-stu-id="42a25-115">Click **OK** to start the cost calculation.</span></span>

6. <span data-ttu-id="42a25-116">في علامة التبويب **تكلفة جدول الصيانة** > في مجموعات جزء الإجراءات **تجميع حسب...**، انقر فوق الأزرار ذات الصلة لعرض مستوى التفاصيل المطلوب لحساب التكلفة.</span><span class="sxs-lookup"><span data-stu-id="42a25-116">On the **Maintenance schedule cost** tab > in the **Group by...** Action Pane groups, click the relevant buttons to show the required detail level of the cost calculation.</span></span> <span data-ttu-id="42a25-117">يتم تمييز أزرار مجموعة جزء الإجراءات المحددة.</span><span class="sxs-lookup"><span data-stu-id="42a25-117">The selected Action Pane group buttons are highlighted.</span></span> <span data-ttu-id="42a25-118">انقر فوق زر لتنشيطه أو إلغاء تنشيطه.</span><span class="sxs-lookup"><span data-stu-id="42a25-118">Click on a button to activate or deactivate it.</span></span>

7. <span data-ttu-id="42a25-119">انقر فوق زر **حساب التكلفة** إذا كنت ترغب في إجراء حساب تكلفة جديد.</span><span class="sxs-lookup"><span data-stu-id="42a25-119">Click the **Calculate cost** button if you want to make a new cost calculation.</span></span>

<span data-ttu-id="42a25-120">يُبين الرسم التوضيحي أدناه نتائج حساب تكلفة جدولة الصيانة.</span><span class="sxs-lookup"><span data-stu-id="42a25-120">The illustration below shows the results of a maintenance schedule cost calculation.</span></span>

![الشكل 1](media/17-preventive-maintenance.png)

