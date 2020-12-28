---
title: تسجيل وقت البدء والتوقف على أمر خدمة
description: تسجيل وقت البدء والتوقف على أمر خدمة.
author: ShylaThompson
manager: tfehr
ms.date: 05/07/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9590a4924442ceccf6f30c35e1dce907f54d368e
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/13/2020
ms.locfileid: "4421038"
---
# <a name="start-and-stop-time-recording-on-a-service-order"></a><span data-ttu-id="e9e92-103">تسجيل وقت البدء والتوقف على أمر خدمة</span><span class="sxs-lookup"><span data-stu-id="e9e92-103">Start and stop time recording on a service order</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="e9e92-104">استخدم هذا الإجراء لبدء تسجيل الوقت وإيقافه لأمر الخدمة التي تم تحديد اتفاقية مستوى الخدمة لها.</span><span class="sxs-lookup"><span data-stu-id="e9e92-104">Use this procedure to start and stop time recording for a service order for which a service level agreement is defined.</span></span>

## <a name="start-time-recording"></a><span data-ttu-id="e9e92-105">بدء تسجيل الوقت</span><span class="sxs-lookup"><span data-stu-id="e9e92-105">Start time recording</span></span>

1.  <span data-ttu-id="e9e92-106">انقر فوق **إدارة الخدمة** \> **عام** \> **أوامر الخدمات** \> **أوامر الخدمات**.</span><span class="sxs-lookup"><span data-stu-id="e9e92-106">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span>

2.  <span data-ttu-id="e9e92-107">انقر فوق علامة تبويب **أمر الخدمة**. وفي **جزء الإجراءات** في مجموعة **اتفاقية مستوى الخدمة**، انقر فوق **بدء**.</span><span class="sxs-lookup"><span data-stu-id="e9e92-107">Click the **Service order** tab. On the **Action Pane**, in the **Service level agreement** group, click **Start**.</span></span>

3.  <span data-ttu-id="e9e92-108">أدخل التاريخ والوقت الذي يجب بدء تسجيل الوقت عنده.</span><span class="sxs-lookup"><span data-stu-id="e9e92-108">Enter the date and time that the time recording should be started.</span></span>

## <a name="stop-time-recording"></a><span data-ttu-id="e9e92-109">إيقاف تسجيل الوقت</span><span class="sxs-lookup"><span data-stu-id="e9e92-109">Stop time recording</span></span>

1.  <span data-ttu-id="e9e92-110">انقر فوق **إدارة الخدمة** \> **عام** \> **أوامر الخدمات** \> **أوامر الخدمات**.</span><span class="sxs-lookup"><span data-stu-id="e9e92-110">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span>

2.  <span data-ttu-id="e9e92-111">انقر فوق علامة تبويب **أمر الخدمة**. وفي **جزء الإجراءات** في مجموعة **اتفاقية مستوى الخدمة**، انقر فوق **إيقاف**.</span><span class="sxs-lookup"><span data-stu-id="e9e92-111">Click the **Service order** tab. On the **Action Pane**, in the **Service level agreement** group, click **Stop**.</span></span>

3.  <span data-ttu-id="e9e92-112">أدخل التاريخ والوقت الذي يجب إيقاف تسجيل الوقت عنده.</span><span class="sxs-lookup"><span data-stu-id="e9e92-112">Enter the date and time that the time recording should be stopped.</span></span>

4.  <span data-ttu-id="e9e92-113">حدد **‏‫إضافة سبب إبطال‬**، ثم حدد كود سبب في القائمة **رمز السبب للمرحلة‬** لتقديم سبب لإيقاف تسجيل الوقت.</span><span class="sxs-lookup"><span data-stu-id="e9e92-113">Select **Add a revocation reason**, and select a reason code in the **Stage reason code** list to provide a reason for stopping the time recording.</span></span>


> [!NOTE]
> <P><span data-ttu-id="e9e92-114">إذا تم تحديد <STRONG>رمز سبب تجاوز الوقت‬</STRONG> في نموذج <STRONG>محددات إدارة الخدمة</STRONG>، فيجب توفير كود سبب لكي يمكنك إيقاف تسجيل الوقت.</span><span class="sxs-lookup"><span data-stu-id="e9e92-114">If <STRONG>Reason code on exceeding time</STRONG> is selected in the <STRONG>Service management parameters</STRONG> form, you must provide a reason code before you can stop the time recording.</span></span></P>



## <a name="see-also"></a><span data-ttu-id="e9e92-115">راجع أيضًا</span><span class="sxs-lookup"><span data-stu-id="e9e92-115">See also</span></span>

<span data-ttu-id="e9e92-116">[‏‏بدء تسجيل وقت اتفاقية مستوى الخدمة (نموذج)](https://technet.microsoft.com/library/hh242297\(v=ax.60\))</span><span class="sxs-lookup"><span data-stu-id="e9e92-116">[Start SLA time recording (form)](https://technet.microsoft.com/library/hh242297\(v=ax.60\))</span></span>

<span data-ttu-id="e9e92-117">[‏‏إيقاف تسجيل وقت اتفاقية مستوى الخدمة (نموذج)](https://technet.microsoft.com/library/hh242241\(v=ax.60\))</span><span class="sxs-lookup"><span data-stu-id="e9e92-117">[Stop SLA time recording (form)](https://technet.microsoft.com/library/hh242241\(v=ax.60\))</span></span>

  


