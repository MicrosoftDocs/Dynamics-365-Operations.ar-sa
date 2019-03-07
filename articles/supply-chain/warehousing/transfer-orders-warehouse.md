---
title: إعداد المستودعات لأوامر التحويل
description: يصف هذا الموضوع كيف يمكنك إعداد المستودعات لأوامر التحويل.
author: Mirzaab
manager: AnnBe
ms.date: 01/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2018-4-30
ms.dyn365.ops.version: 8
ms.openlocfilehash: 8111601cb2948c66097b0f5b2f261b7462b279f9
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/29/2019
ms.locfileid: "337453"
---
# <a name="set-up-warehouses-for-transfer-orders"></a><span data-ttu-id="eeed9-103">إعداد المستودعات لأوامر التحويل</span><span class="sxs-lookup"><span data-stu-id="eeed9-103">Set up warehouses for transfer orders</span></span> 

[!include [banner](../includes/banner.md)]

<span data-ttu-id="eeed9-104">يُمكنك استخدام مستويات المستودع لإنشاء تدرج هرمي يدعم أوامر التحويل بين المستودعات.</span><span class="sxs-lookup"><span data-stu-id="eeed9-104">You can use warehouse levels to create a hierarchy that supports transfer orders between warehouses.</span></span> <span data-ttu-id="eeed9-105">وبناءً على هذا الإعداد، تقوم الجدولة الرئيسية بجساب متطلبات الأصناف في مستوى مستودع فريد وتقوم بإنشاء أوامر النقل المخططة من مستودع المصدر الذي تم تعيينه لتحقيقها.</span><span class="sxs-lookup"><span data-stu-id="eeed9-105">Based on this setup, master scheduling calculates item requirements at the individual warehouse level and generates planned transfer orders from an assigned source warehouse to fulfill them.</span></span>

1.  <span data-ttu-id="eeed9-106">انقر فوق **إدارة المخزون > إعداد > تصنيف المخزون > المستودعات**.</span><span class="sxs-lookup"><span data-stu-id="eeed9-106">Click **Inventory management > Setup > Inventory breakdown > Warehouses**.</span></span>

2.  <span data-ttu-id="eeed9-107">حدد المستودع الذي تريد إعادة ملئه.</span><span class="sxs-lookup"><span data-stu-id="eeed9-107">Select the warehouse that you want to refill.</span></span>

3.  <span data-ttu-id="eeed9-108">على علامة التبويب السريعة **التخطيط الرئيسي**، حدد خانة الاختيار **إعادة ملء**.</span><span class="sxs-lookup"><span data-stu-id="eeed9-108">On the **Master planning** FastTab, select the **Refilling** check box.</span></span>

4.  <span data-ttu-id="eeed9-109">في الحقل **المستودع الرئيسي**، حدد المستودع الذي تريد تعيينه كمستودع لإعادة الملء.</span><span class="sxs-lookup"><span data-stu-id="eeed9-109">In the **Main warehouse** field, select the warehouse that you want to assign as the refilling warehouse.</span></span> <span data-ttu-id="eeed9-110">تقوم الجدولة الرئيسية بحساب متطلبات التحويل للمستودع المحدد، ثم تنشئ أمر تحويل مخطط من **المستودع الرئيسي** المعين.</span><span class="sxs-lookup"><span data-stu-id="eeed9-110">Master scheduling calculates a transfer requirement for the selected warehouse and generates a planned transfer order from the assigned **Main warehouse**.</span></span>
   
    > [!NOTE]
    > <P><span data-ttu-id="eeed9-111">إذا ألغيت تحديد خانة الاختيار <STRONG>إعادة ملء</STRONG>، فسيتم تعيين المستودع المحدد لمستوى مستودع حسب <STRONG>المستودع الرئيسي</STRONG>، ومع ذلك لن يتم إعداد <STRONG>المستودع الرئيسي</STRONG> كمستودع لإعادة الملء.</span><span class="sxs-lookup"><span data-stu-id="eeed9-111">If you clear the <STRONG>Refilling</STRONG> check box, the selected warehouse is assigned a warehouse level in regard to the <STRONG>Main warehouse</STRONG>, but the <STRONG>Main warehouse</STRONG> is not set up as a refilling warehouse.</span></span></P>

5.  <span data-ttu-id="eeed9-112">أغلق الصفحة لتطبيق الإعداد الجديد.</span><span class="sxs-lookup"><span data-stu-id="eeed9-112">Close the page to apply the new setup.</span></span>


> [!TIP]
> <P><span data-ttu-id="eeed9-113">إذا أردت تعيين مستودع لإعادة الملء، فيجب أولاً إعداد المستودع كبُعد تخزين في صفحة <STRONG>مجموعات أبعاد التخزين</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="eeed9-113">If you want to assign a warehouse for refilling, you must first set up the warehouse as a storage dimension on the <STRONG>Storage dimension groups</STRONG> page.</span></span> <span data-ttu-id="eeed9-114">في هذه الصفحة، حدد الحقل <STRONG>انشط</STRONG> والحقل <STRONG>خطة التغطية حسب البُعد‬</STRONG> للمستودع.</span><span class="sxs-lookup"><span data-stu-id="eeed9-114">On this page, select the <STRONG>Active</STRONG> field and the <STRONG>Coverage plan by dimension</STRONG> field for the warehouse.</span></span></P>

## <a name="set-up-transport-lead-time"></a><span data-ttu-id="eeed9-115">إعداد وقت إعداد البضائع لنقلها</span><span class="sxs-lookup"><span data-stu-id="eeed9-115">Set up transport lead time</span></span>

<span data-ttu-id="eeed9-116">يجب أيضًا إعداد وقت إعداد البضائع لنقلها بين المستودعات في صفحة **أيام النقل**.</span><span class="sxs-lookup"><span data-stu-id="eeed9-116">You must also set up the transport lead time between the warehouses on the **Transport days** page.</span></span> 
1. <span data-ttu-id="eeed9-117">انتقل إلى **إدارة المخزون > الإعداد > التوزيع > أيام النقل**.</span><span class="sxs-lookup"><span data-stu-id="eeed9-117">Go to **Inventory management > Setup > Distribution > Transport days**.</span></span>
2. <span data-ttu-id="eeed9-118">في حقل **نقطة الاستلام‬**، حدد **المستودع**.</span><span class="sxs-lookup"><span data-stu-id="eeed9-118">In the **Receiving point** field, select **warehouse**.</span></span>
3. <span data-ttu-id="eeed9-119">حدد **مستودع الشحن** و**مستودع الاستلام** و**أيام النقل**.</span><span class="sxs-lookup"><span data-stu-id="eeed9-119">Select the **Shipping warehouse**, **Receiving warehouse**, and **Transport days**.</span></span> 
4. <span data-ttu-id="eeed9-120">(اختياري) يمكنك أيضًا تعيين وقت النقل، وفقًا لوضع التسليم، ضمن علامة التبويب **عدد أيام النقل حسب وضع التسليم‬**.</span><span class="sxs-lookup"><span data-stu-id="eeed9-120">(Optional) You can also set transport time, depending on the mode of delivery, under the **Transport days per mode of delivery** tab.</span></span>
