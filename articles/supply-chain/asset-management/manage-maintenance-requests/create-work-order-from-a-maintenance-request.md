---
title: إنشاء أوامر عمل من طلبات الصيانة
description: يشرح هذا الموضوع كيفية إنشاء أمر عمل من طلب صيانة في إدارة الأصول.
author: josaw1
manager: tfehr
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 5bf147104909302173c32b8376f16c66784110cb
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5253316"
---
# <a name="create-work-orders-from-maintenance-requests"></a><span data-ttu-id="57ab0-103">إنشاء أوامر عمل من طلبات الصيانة</span><span class="sxs-lookup"><span data-stu-id="57ab0-103">Create work orders from maintenance requests</span></span>

[!include [banner](../../includes/banner.md)]

 


<span data-ttu-id="57ab0-104">بعد إنشاء طلبات الصيانة، يمكنك تحويلها بسهولة إلى أوامر عمل.</span><span class="sxs-lookup"><span data-stu-id="57ab0-104">After you've created maintenance requests, you can easily convert them to work orders.</span></span> <span data-ttu-id="57ab0-105">يصف هذا الموضوع أسرع طريقة للعمل مع طلبات الصيان، وتحديث طلبات صيانة متعددة في الوقت نفسه، ثم إنشاء أمر عمل للعديد من طلبات الصيانة في نفس الوقت.</span><span class="sxs-lookup"><span data-stu-id="57ab0-105">This topic describes the quickest way to work with maintenance requests, update several maintenance requests at the same time, and then create a work order for several maintenance requests at the same time.</span></span> <span data-ttu-id="57ab0-106">في صفحة **طلبات الصيانة النشطة** أو **طلبات الصيانة الخاصة بموقع العمل لدي**، يمكنك أيضًا العمل مع طلب صيانة واحد في كل مرة وتحويل طلب صيانة إلى أمر عمل.</span><span class="sxs-lookup"><span data-stu-id="57ab0-106">On the **Active maintenance requests** or **My functional location maintenance requests** page, you can also work with one maintenance request at a time and convert one maintenance request to a work order.</span></span>

> [!NOTE]
> <span data-ttu-id="57ab0-107">ويمكن ربط كل طلب صيانة أمر عمل واحد فقط.</span><span class="sxs-lookup"><span data-stu-id="57ab0-107">Every maintenance request can be related to only one work order.</span></span> <span data-ttu-id="57ab0-108">ومع ذلك، يمكن تضمين طلبات صيانة متعددة في أمر عمل واحد، حتى في حال وجود أصول مختلفة لطلبات الصيانة.</span><span class="sxs-lookup"><span data-stu-id="57ab0-108">However, multiple maintenance requests can be included in one work order, even if the maintenance requests have different assets.</span></span>

1. <span data-ttu-id="57ab0-109">حدد **إدارة الأصول** \> **عام** \> **طلبات الصيانة** \> **جميع طلبات الصيانة**.</span><span class="sxs-lookup"><span data-stu-id="57ab0-109">Select **Asset management** \> **Common** \> **maintenance requests** \> **All maintenance requests**.</span></span>
2. <span data-ttu-id="57ab0-110">قبل إنشاء أمر عمل من طلبات الصيانة، يجب عليك تحديد نوع مهمة صيانة لطلبات الصيانة كحدٍ أدنى، وكذلك متغيرات نوع مهمة الصيانة ووظيفة تحتاج إلى تدريبات معينة، إذا كانت هذه المعلومات ذات صلة.</span><span class="sxs-lookup"><span data-stu-id="57ab0-110">Before you can create a work order from maintenance requests, you must select, at a minimum, a maintenance job type for the maintenance requests, and also a maintenance job type variant and trade, if this information is relevant.</span></span> <span data-ttu-id="57ab0-111">في طريقه عرض الشبكة، يمكنك تحديث المعلومات بسهولة لطلب الصيانة.</span><span class="sxs-lookup"><span data-stu-id="57ab0-111">In the grid view, you can easily update information for a maintenance request.</span></span>
3. <span data-ttu-id="57ab0-112">عندما تصبح جاهزًا لإنشاء أمر عمل، حدد طلبات الصيانة المراد تضمينها به.</span><span class="sxs-lookup"><span data-stu-id="57ab0-112">When you're ready to create a work order, select the maintenance requests to include in it.</span></span>

    - <span data-ttu-id="57ab0-113">إذا قمت بتحديد العديد من طلبات الصيانة لتحويلها إلى أمر عمل، فيجب تعيين حقل **الأصل** وحقل **نوع مهمة الصيانة** قبل إنشاء أمر العمل.</span><span class="sxs-lookup"><span data-stu-id="57ab0-113">If you select several maintenance requests to convert to a work order, both the **Asset** field and the **Maintenance job type** field must be set before you create the work order.</span></span>
    - <span data-ttu-id="57ab0-114">في حالة تحديد طلب صيانة واحد لتحويله إلى أمر عمل ، فيجب تعيين حقل **الأصل** فقط قبل إنشاء أمر العمل.</span><span class="sxs-lookup"><span data-stu-id="57ab0-114">If you select one maintenance request to convert to a work order, only the **Asset** field must be set before you create the work order.</span></span> <span data-ttu-id="57ab0-115">ومع ذلك، عند إنشاء أمر العمل، يمكنك تحديد نوع مهمة صيانة (ونوع متغير مهمة صيانة ذات صلة ووظيفة تحتاج إلى تدريبات، إذا كانت هذه المعلومات ذات صلة) في مربع الحوار **إنشاء أمر عمل**.</span><span class="sxs-lookup"><span data-stu-id="57ab0-115">However, when you create the work order, you can select a maintenance job type (and a related maintenance job type variant and trade, if this information is relevant) in the **Create work order** dialog box.</span></span>

4. <span data-ttu-id="57ab0-116">حدد **أمر عمل**.</span><span class="sxs-lookup"><span data-stu-id="57ab0-116">Select **Work order**.</span></span>
5. <span data-ttu-id="57ab0-117">في مربع الحوار **إنشاء أمر عمل**، قم بتعيين الحقول ، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="57ab0-117">In the **Create work order** dialog box, set the fields, and then select **OK**.</span></span>

    <span data-ttu-id="57ab0-118">قد يعلمك شريط رسالة بإنشاء أمر عمل جديد.</span><span class="sxs-lookup"><span data-stu-id="57ab0-118">A message bar might notify you that a new work order has been created.</span></span>

    <span data-ttu-id="57ab0-119">بالإضافة إلى ذلك، عند إنشاء أمر عمل يستند إلى طلب صيانة، إذا تم تضمين الأصل المرتبط بطلب الصيانة في اتفاقيه ضمان، فسيعلمك شريط رسالة، عن اتفاقيه الضمان.</span><span class="sxs-lookup"><span data-stu-id="57ab0-119">Additionally, when you create a work order that is based on a maintenance request, if the asset that is related to the maintenance request is included in a warranty agreement, a message bar notifies you about the warranty agreement.</span></span>

6. <span data-ttu-id="57ab0-120">حدد **إدارة الأصول** \> **عام** \> **أوامر العمل** \> **جميع أوامر العمل**، وافتح أمر العمل الجديد.</span><span class="sxs-lookup"><span data-stu-id="57ab0-120">Select **Asset management** \> **Common** \> **Work orders** \> **All work orders**, and open the new work order.</span></span>

    ![فتح أمر عمل جديد](media/05-manage-maintenance-requests.png)



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]