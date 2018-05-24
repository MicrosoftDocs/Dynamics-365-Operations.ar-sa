---
title: "إعداد فني مفضل"
description: "يمكنك تحديد أي عامل كفني مفضل لاتفاقية خدمة أو طلب خدمة."
author: YuyuScheller
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAAgreementTable, SMADispatchBoard
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
ms.openlocfilehash: 390e436b63fdfe82e0b743e7f286cae3bb29be55
ms.contentlocale: ar-sa
ms.lasthandoff: 05/08/2018

---


# <a name="set-up-a-preferred-technician"></a><span data-ttu-id="9f815-103">إعداد فني مفضل</span><span class="sxs-lookup"><span data-stu-id="9f815-103">Set up a preferred technician</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="9f815-104">يمكنك تحديد أي عامل كفني مفضل لاتفاقية خدمة أو طلب خدمة.</span><span class="sxs-lookup"><span data-stu-id="9f815-104">You can select any worker as a preferred technician for a service agreement or service order.</span></span> <span data-ttu-id="9f815-105">وبالرغم من هذا، فمن الأفضل إضافة العامل إلى فريق الإرسال المناسب كي يتم تضمين العامل في **لوحة الإرسال**.</span><span class="sxs-lookup"><span data-stu-id="9f815-105">However, it is a good idea to add the worker to the appropriate dispatch team so that the worker is included on the **Dispatch board**.</span></span>

## <a name="assign-employee-to-a-dispatch-team"></a><span data-ttu-id="9f815-106">تعيين موظف لفريق إرسال</span><span class="sxs-lookup"><span data-stu-id="9f815-106">Assign employee to a dispatch team</span></span>

1.  <span data-ttu-id="9f815-107">انقر فوق **الموارد البشرية** \> **عام** \> **العاملون** \> **العاملون**.</span><span class="sxs-lookup"><span data-stu-id="9f815-107">Click **Human resources** \> **Common** \> **Workers** \> **Workers**.</span></span> <span data-ttu-id="9f815-108">انقر نقرًا مزدوجًا فوق عامل لفتح صفحة تفاصيل العامل.</span><span class="sxs-lookup"><span data-stu-id="9f815-108">Double-click a worker to open the worker details page.</span></span> <span data-ttu-id="9f815-109">في **جزء الإجراءات**، انقر فوق **الإعداد** \> **فريق الإرسال** لفتح النموذج **إرسال العاملين**.</span><span class="sxs-lookup"><span data-stu-id="9f815-109">On the **Action Pane**, click **Setup** \>**Dispatch team** to open the **Dispatch workers** form.</span></span>

2.  <span data-ttu-id="9f815-110">في الحقل **فريق الإرسال**، حدد الفريق المراد تعيين العامل إليه.</span><span class="sxs-lookup"><span data-stu-id="9f815-110">In the **Dispatch team** field, select the team to assign the worker to.</span></span>

## <a name="assign-a-preferred-technician-to-a-service-agreement"></a><span data-ttu-id="9f815-111">تعيين فني مُفضل لاتفاقية خدمة</span><span class="sxs-lookup"><span data-stu-id="9f815-111">Assign a preferred technician to a service agreement</span></span>

1.  <span data-ttu-id="9f815-112">انقر فوق **إدارة الخدمة** \> **عام** \> **اتفاقيات الخدمة‬** \> **اتفاقيات الخدمة‬**.</span><span class="sxs-lookup"><span data-stu-id="9f815-112">Click **Service management** \> **Common** \> **Service agreements** \> **Service agreements**.</span></span> <span data-ttu-id="9f815-113">انقر نقرًا مزدوجًا فوق اتفاقية خدمة لفتح نموذج التفاصيل.</span><span class="sxs-lookup"><span data-stu-id="9f815-113">Double-click a service agreement to open the details form.</span></span>

2.  <span data-ttu-id="9f815-114">في علامة التبويب **عام**، حدد الحقل **الفني المفضل**، ثم حدد عضوًا في فريق الإرسال المناسب على أنه فني مفضل لاتفاقية الخدمة.</span><span class="sxs-lookup"><span data-stu-id="9f815-114">On the **General** tab, select the **Preferred technician** field, and then select a member of the appropriate dispatch team as the preferred technician for the service agreement.</span></span>

## <a name="assign-a-preferred-technician-to-a-service-order"></a><span data-ttu-id="9f815-115">تعيين فني مُفضل لأمر خدمة</span><span class="sxs-lookup"><span data-stu-id="9f815-115">Assign a preferred technician to a service order</span></span>

1.  <span data-ttu-id="9f815-116">انقر فوق **إدارة الخدمة** \> **دوري** \> **لوحة الإرسال‬**.</span><span class="sxs-lookup"><span data-stu-id="9f815-116">Click **Service management** \> **Periodic** \> **Dispatch board**.</span></span>
    

    > [!NOTE]
    > <P><span data-ttu-id="9f815-117">في النموذج <STRONG>لوحة الإرسال</STRONG>، قم بتعيين نطاق زمني لأنشطة الإرسال المراد عرضها.</span><span class="sxs-lookup"><span data-stu-id="9f815-117">In the <STRONG>Dispatch board</STRONG> form, specify a date range for dispatch activities to view.</span></span> <span data-ttu-id="9f815-118">وبالإضافة إلى ذلك، حدد سواءً كنت تريد عرض الأنشطة المغلقة وسواءً كنت تريد حصر قائمة أنشطة الإرسال على الفرق التي تنتمي إليها أو الفرق المخول لها بالمراقبة.</span><span class="sxs-lookup"><span data-stu-id="9f815-118">Also, specify whether to display closed activities and whether to limit the dispatch activity list to teams that you belong to or are authorized to monitor.</span></span> <span data-ttu-id="9f815-119">انقر فوق <STRONG>موافق</STRONG> لفتح <STRONG>لوحة الإرسال</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="9f815-119">Click <STRONG>OK</STRONG> to open the <STRONG>Dispatch board</STRONG>.</span></span></P>



2.  <span data-ttu-id="9f815-120">حدد بند نشاط الخدمة المراد تعديله.</span><span class="sxs-lookup"><span data-stu-id="9f815-120">Select the line of the service activity to modify.</span></span>

3.  <span data-ttu-id="9f815-121">من علامة التبويب **ذو صلة**، استخدم قائمة **العامل** لتعيين عضو لفريق الإرسال الملائم كفني مُفضل لاستدعاء الخدمة.</span><span class="sxs-lookup"><span data-stu-id="9f815-121">On the **Related** tab, use the **Worker** list to assign a member of the appropriate dispatch team as the preferred technician for the service call.</span></span>

## <a name="see-also"></a><span data-ttu-id="9f815-122">راجع أيضًا</span><span class="sxs-lookup"><span data-stu-id="9f815-122">See also</span></span>

[<span data-ttu-id="9f815-123">اتفاقيات الخدمة</span><span class="sxs-lookup"><span data-stu-id="9f815-123">Service agreements</span></span>](service-agreements.md)

[<span data-ttu-id="9f815-124">إنشاء أوامر خدمة يدويًا</span><span class="sxs-lookup"><span data-stu-id="9f815-124">Create service orders manually</span></span>](create-service-orders-manually.md)

<span data-ttu-id="9f815-125">[اتفاقيات الخدمات (نموذج)](https://technet.microsoft.com/en-us/library/aa617823\(v=ax.60\))</span><span class="sxs-lookup"><span data-stu-id="9f815-125">[Service agreements (form)](https://technet.microsoft.com/en-us/library/aa617823\(v=ax.60\))</span></span>
  



