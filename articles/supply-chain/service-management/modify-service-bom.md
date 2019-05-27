---
title: تعديل شجرة مواد الخدمة
description: تعديل قائمة مكونات صنف.
author: ShylaThompson
manager: AnnBe
ms.date: 05/03/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAAgreementTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6a66f7ea7b30e033a39c292dff4064deef6bff4c
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/15/2019
ms.locfileid: "1570332"
---
# <a name="modify-a-service-bom"></a><span data-ttu-id="876d8-103">تعديل شجرة مواد الخدمة</span><span class="sxs-lookup"><span data-stu-id="876d8-103">Modify a Service BOM</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="876d8-104">يمكنك تسجيل سجل عنصر داخل BOM لخدمة ما.</span><span class="sxs-lookup"><span data-stu-id="876d8-104">You can record the history of an element in a service BOM.</span></span> <span data-ttu-id="876d8-105">وفي كل مرة تقوم فيها بتحديث بند قائمة مكونات صنف، يتم إنشاء بند سجل في الجزء **المحفوظات**.</span><span class="sxs-lookup"><span data-stu-id="876d8-105">Every time that you update a BOM line, a history line is created in the **History** pane.</span></span> <span data-ttu-id="876d8-106">يُظهر بند السجل الحالة الحالية لبند BOM.</span><span class="sxs-lookup"><span data-stu-id="876d8-106">The history line shows the current state of the BOM line.</span></span>

## <a name="update-a-service-bom-element"></a><span data-ttu-id="876d8-107">تحديث عنصر شجرة مواد الخدمة</span><span class="sxs-lookup"><span data-stu-id="876d8-107">Update a service BOM element</span></span>

1.  <span data-ttu-id="876d8-108">انقر فوق **إدارة الخدمة** \> **عام** \> **اتفاقيات الخدمة‬** \> **اتفاقيات الخدمة‬**.</span><span class="sxs-lookup"><span data-stu-id="876d8-108">Click **Service management** \> **Common** \> **Service agreements** \> **Service agreements**.</span></span>

2.  <span data-ttu-id="876d8-109">انقر فوق **تحرير** لفتح نموذج تفاصيل **اتفاقيات الخدمة**.</span><span class="sxs-lookup"><span data-stu-id="876d8-109">Click **Edit** to open the **Service agreements** details form.</span></span>

3.  <span data-ttu-id="876d8-110">في **جزء الإجراءات**، انقر فوق **كائنات الخدمة** لفتح النموذج **كائنات الخدمة**.</span><span class="sxs-lookup"><span data-stu-id="876d8-110">On the **Action Pane**, click **Service objects** to open the **Service objects** form.</span></span>

4.  <span data-ttu-id="876d8-111">حدد الكائن الذي تريد تحديث بند قائمة مكونات الصنف له، ثم انقر فوق **المصمم**.</span><span class="sxs-lookup"><span data-stu-id="876d8-111">Select the object to update a BOM line for, and then click **Designer**.</span></span>

5.  <span data-ttu-id="876d8-112">في نموذج **المصمم**، حدد بند قائمة مكونات الصنف المراد تحديثه، ثم انقر فوق **تحرير بند قائمة مكونات الصنف**.</span><span class="sxs-lookup"><span data-stu-id="876d8-112">In the **Designer** form, select the BOM line to update, and then click **Edit BOM line**.</span></span>
    
    > [!NOTE]
    > <P><span data-ttu-id="876d8-113">في علامة التبويب <STRONG>إعداد</STRONG>، حدد خانة الاختيار <STRONG>تحرير عند الإضافة</STRONG> إذا كنت ترغب في فتح النموذج <STRONG>تحرير بند قائمة مكونات الصنف</STRONG> عند سحب بند إلى قائمة مكونات نصف خدمة.</span><span class="sxs-lookup"><span data-stu-id="876d8-113">On the <STRONG>Setup</STRONG> tab, select the <STRONG>Edit when adding</STRONG> check box if you want the <STRONG>Edit BOM line</STRONG> form to open when you drag a line into the service BOM.</span></span></P>

6.  <span data-ttu-id="876d8-114">في حقل **الكمية**، ثم أدخل الكمية.</span><span class="sxs-lookup"><span data-stu-id="876d8-114">In the **Quantity** field, enter the quantity.</span></span>

7.  <span data-ttu-id="876d8-115">إذا كنت ترغب في إنشاء بند أمر خدمة لصنف الاستبدال، والذي يمكن عندئذٍ فوترته، حدد خانة الاختيار **إنشاء بند أمر خدمة**.</span><span class="sxs-lookup"><span data-stu-id="876d8-115">If you want to create a service order line for the replacement item, which can then be invoiced, select the **Create service order line** check box.</span></span>

8.  <span data-ttu-id="876d8-116">انقر فوق **موافق** لإغلاق النموذج.</span><span class="sxs-lookup"><span data-stu-id="876d8-116">Click **OK** to close the form.</span></span>

## <a name="delete-a-service-bom-line"></a><span data-ttu-id="876d8-117">حذف بند شجرة مواد خدمة</span><span class="sxs-lookup"><span data-stu-id="876d8-117">Delete a service BOM line</span></span>

1.  <span data-ttu-id="876d8-118">انقر فوق **إدارة الخدمة** \> **عام** \> **اتفاقيات الخدمة‬** \> **اتفاقيات الخدمة‬**.</span><span class="sxs-lookup"><span data-stu-id="876d8-118">Click **Service management** \> **Common** \> **Service agreements** \> **Service agreements**.</span></span>

2.  <span data-ttu-id="876d8-119">انقر فوق **تحرير** لفتح نموذج تفاصيل **اتفاقيات الخدمة**.</span><span class="sxs-lookup"><span data-stu-id="876d8-119">Click **Edit** to open the **Service agreements** details form.</span></span>

3.  <span data-ttu-id="876d8-120">في **جزء الإجراءات**، انقر فوق **كائنات الخدمة** لفتح النموذج **كائنات الخدمة**.</span><span class="sxs-lookup"><span data-stu-id="876d8-120">On the **Action Pane**, click **Service objects** to open the **Service objects** form.</span></span>

4.  <span data-ttu-id="876d8-121">حدد الكائن الذي ترغب في حذف بند قائمة مكونات صنف خدمة منه، ثم انقر فوق **المصمم**.</span><span class="sxs-lookup"><span data-stu-id="876d8-121">Select the object to delete a service BOM line from, and then click **Designer**.</span></span>

5.  <span data-ttu-id="876d8-122">في نموذج **المصمم**، حدد بند قائمة مكونات الصنف المراد حذفه، ثم انقر فوق **حذف بند قائمة مكونات الصنف**.</span><span class="sxs-lookup"><span data-stu-id="876d8-122">In the **Designer** form, select the BOM line to delete, and then click **Delete BOM line**.</span></span>

## <a name="see-also"></a><span data-ttu-id="876d8-123">راجع أيضًا</span><span class="sxs-lookup"><span data-stu-id="876d8-123">See also</span></span>

[<span data-ttu-id="876d8-124">شجرة المواد القالب </span><span class="sxs-lookup"><span data-stu-id="876d8-124">Template BOMs</span></span>](template-boms.md)

  


