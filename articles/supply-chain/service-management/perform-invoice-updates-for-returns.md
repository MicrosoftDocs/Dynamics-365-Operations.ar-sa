---
title: "إجراء تحديثات الفاتورة للمرتجعات"
description: "تدعم هذه الوظائف العمليات التجارية للمؤسسات التي تختار إعداد فواتير أوامر الإرجاع وأوامر المبيعات لها في نفس الوقت وبواسطة نفس الشخص."
author: YuyuScheller
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 53ae1c3bda06d07a0ca633981ddd46092eae507e
ms.contentlocale: ar-sa
ms.lasthandoff: 05/08/2018

---


# <a name="perform-invoice-updates-for-returns"></a><span data-ttu-id="5ba1b-103">إجراء تحديثات الفاتورة للمرتجعات</span><span class="sxs-lookup"><span data-stu-id="5ba1b-103">Perform invoice updates for returns</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="5ba1b-104">يعتبر أمر الإرجاع بمثابة نوع من أمر المبيعات الذي يتم تمييزه على أنه الأمر المرجع.</span><span class="sxs-lookup"><span data-stu-id="5ba1b-104">A return order is a type of sales order that is marked as a returned order.</span></span> <span data-ttu-id="5ba1b-105">لذلك، يتم استخدام صفحة قائمة **كافة أوامر المبيعات** لإنشاء فواتير لأوامر الإرجاع بدلاً من النموذج **أوامر الإرجاع**.</span><span class="sxs-lookup"><span data-stu-id="5ba1b-105">Therefore, the **All sales orders** list page is used to generate invoices for return orders instead of the **Return orders** form.</span></span> <span data-ttu-id="5ba1b-106">تدعم هذه الوظائف العمليات التجارية للمؤسسات التي تختار إعداد فواتير أوامر الإرجاع وأوامر المبيعات لها في نفس الوقت وبواسطة نفس الشخص.</span><span class="sxs-lookup"><span data-stu-id="5ba1b-106">This functionality supports the business processes of organizations that choose to have return orders and sales orders invoiced at the same time and by the same person.</span></span>

<span data-ttu-id="5ba1b-107">نظراً لأن الفاتورة الخاصة بصنف مرتجع تكون بمبلغ سالب، فهي تسمى إشعار دائن.</span><span class="sxs-lookup"><span data-stu-id="5ba1b-107">Because the invoice for a returned item is for a negative amount, it is called a credit note.</span></span>

<span data-ttu-id="5ba1b-108">عند إعداد تحديث الفاتورة لمعالجة المجموعة، يجب أن يكون لأمر المبيعات من نوع **الأمر المرجع** بند مرتجع بالحالة **مستلم**، والذي يشير إلى أنه تم تحديث كشف التعبئة الخاص بالأمر.</span><span class="sxs-lookup"><span data-stu-id="5ba1b-108">When you set up the invoice update for batch processing, the sales order of type **Returned order** must have a return line status of **Received**, which indicates that the order's packing slip has been updated.</span></span>

## <a name="post-an-invoice-for-a-return-order"></a><span data-ttu-id="5ba1b-109">ترحيل فاتورة لأمر مرتجع</span><span class="sxs-lookup"><span data-stu-id="5ba1b-109">Post an invoice for a return order</span></span>

1.  <span data-ttu-id="5ba1b-110">انقر فوق **حسابات مدينة** \> **عام** \> **أوامر المبيعات** \> **كل أوامر المبيعات**.</span><span class="sxs-lookup"><span data-stu-id="5ba1b-110">Click **Accounts receivable** \> **Common** \> **Sales orders** \> **All sales orders**.</span></span>

2.  <span data-ttu-id="5ba1b-111">حدد أمر مبيعات والذي يتم عرض **الأمر المرجع** له في الحقل **نوع أمر**.</span><span class="sxs-lookup"><span data-stu-id="5ba1b-111">Select a sales order for which **Returned order** is displayed in the **Order type** field.</span></span>

3.  <span data-ttu-id="5ba1b-112">في جزء الإجراءات، في علامة التبويب **الفاتورة**، في المجموعة **إنشاء**، انقر فوق **فاتورة**.</span><span class="sxs-lookup"><span data-stu-id="5ba1b-112">On the Action Pane, on the **Invoice** tab, in the **Generate** group, click **Invoice**.</span></span>

4.  <span data-ttu-id="5ba1b-113">في علامة تبويب **المعلمات**، حدد خانة الاختيار **ترحيل**.</span><span class="sxs-lookup"><span data-stu-id="5ba1b-113">On the **Parameters** tab, select the **Posting** check box.</span></span>

5.  <span data-ttu-id="5ba1b-114">راجع المعلومات الموجودة في النموذج وقم أي تغييرات ضرورية.</span><span class="sxs-lookup"><span data-stu-id="5ba1b-114">Review information in the form and make any changes that are needed.</span></span>

6.  <span data-ttu-id="5ba1b-115">وانقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="5ba1b-115">Click **OK**.</span></span> <span data-ttu-id="5ba1b-116">تم ترحيل إشعار الدائن.</span><span class="sxs-lookup"><span data-stu-id="5ba1b-116">The credit note is posted.</span></span>

## <a name="see-also"></a><span data-ttu-id="5ba1b-117">راجع أيضًا</span><span class="sxs-lookup"><span data-stu-id="5ba1b-117">See also</span></span>

[<span data-ttu-id="5ba1b-118">تحديثات كشف التعبئة للمرتجعات</span><span class="sxs-lookup"><span data-stu-id="5ba1b-118">Packing slip updates for returns</span></span>](packing-slip-updates-returns.md)

  



