---
title: تأكيد جداول دفع تأجير الأصول في دُفعة
description: يوضح هذا الموضوع كيفية تأكيد جداول دفع متعددة في دُفعة.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 9c680ea16e9f64107fde081c7e7763697356dcc1
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "4971368"
---
# <a name="confirm-asset-leasing-payment-schedules-in-a-batch"></a><span data-ttu-id="7d855-103">تأكيد جداول دفع تأجير الأصول في دُفعة</span><span class="sxs-lookup"><span data-stu-id="7d855-103">Confirm Asset leasing payment schedules in a batch</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7d855-104">يوضح هذا الموضوع كيفية تأكيد جداول دفع متعددة في دُفعة.</span><span class="sxs-lookup"><span data-stu-id="7d855-104">This topic explains how to confirm multiple payment schedules in a batch.</span></span> <span data-ttu-id="7d855-105">يتم تأكيد جداول الدُفعة إما على أساس عقد الإيجار لعقد الإيجار أو من خلال عملية دُفعة التأكيد.</span><span class="sxs-lookup"><span data-stu-id="7d855-105">Payment schedules are confirmed either on a lease-to-lease basis or through the confirmation batch process.</span></span> <span data-ttu-id="7d855-106">لا يمكن ترحيل إدخال دفتر اليومية إلا مقابل عقد إيجار يحتوي على جدول دفع مؤكد.</span><span class="sxs-lookup"><span data-stu-id="7d855-106">A journal entry can be posted only against a lease that has a confirmed payment schedule.</span></span> <span data-ttu-id="7d855-107">ويعمل تأكيد جدول الدفعة كاعتماد نهائي للمعلومات المالية الخاصة بعقد الإيجار.</span><span class="sxs-lookup"><span data-stu-id="7d855-107">Confirmation of the payment schedule serves as a final approval of the financial information for the lease.</span></span> <span data-ttu-id="7d855-108">تشكل كافة التغييرات المستقبلية للمعلومات المالية الخاصة بعقد الإيجار، مثل المدفوعات وفترة الإيجار، تسوية عقد الإيجار ويجب معالجتها بتلك الطريقة.</span><span class="sxs-lookup"><span data-stu-id="7d855-108">All future changes to the financial information for the lease, such as payments and the lease term, constitute a lease adjustment and should be processed in that way.</span></span>

<span data-ttu-id="7d855-109">لتأكيد جداول الدفع المتعددة، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="7d855-109">To confirm multiple payment schedules, follow these steps.</span></span>

1. <span data-ttu-id="7d855-110">انتقل إلى **تأجير الأصول \> دوري \> دُفعة التأكيد**.</span><span class="sxs-lookup"><span data-stu-id="7d855-110">Go to **Asset leasing \> Periodic \> Confirmation batch**.</span></span>
2. <span data-ttu-id="7d855-111">في الصفحة **دُفعة التأكيد**، حدد **دفعة التأكيد**.</span><span class="sxs-lookup"><span data-stu-id="7d855-111">On the **Confirmation batch** page, select **Confirmation batch**.</span></span>
3. <span data-ttu-id="7d855-112">في مربع الحوار الذي يظهر، قم بتصفية الدفاتر التي ترغب في تأكيدها.</span><span class="sxs-lookup"><span data-stu-id="7d855-112">In the dialog box that appears, filter for the books that you want to confirm.</span></span>

    - <span data-ttu-id="7d855-113">لتأكيد كافة الدفاتر في مجموعة عقد إيجار معينة، حدد المجموعة في الحقل **مجموعة عقد الإيجار**.</span><span class="sxs-lookup"><span data-stu-id="7d855-113">To confirm all the books in a specific lease group, select the group in the **Lease group** field.</span></span>
    - <span data-ttu-id="7d855-114">لتأكيد دفاتر محددة، حدد الدفاتر الموجودة في الحقل **معرف الدفتر**.</span><span class="sxs-lookup"><span data-stu-id="7d855-114">To confirm specific books, select the books in the **Book ID** field.</span></span>
    - <span data-ttu-id="7d855-115">لتأكيد كافة الدفاتر، قم بتشغيل المعلمة **لكافة دفاتر**.</span><span class="sxs-lookup"><span data-stu-id="7d855-115">To confirm all books, turn on the **For all books** parameter.</span></span>

<span data-ttu-id="7d855-116">تظهر معلومات الدفاتر التي تم تأكيدها حديثًا في الصفحة **الدفاتر المؤكدة**.</span><span class="sxs-lookup"><span data-stu-id="7d855-116">Information for the newly confirmed books is shown on the **Confirmed books** page.</span></span> <span data-ttu-id="7d855-117">بعد تأكيد جداول الدفع، فإنه يمكن ترحيل إدخالات دفتر يومية التقييم الأولي مقابل عقود الإيجار.</span><span class="sxs-lookup"><span data-stu-id="7d855-117">After the payment schedules are confirmed, the initial recognition journal entries can be posted against the leases.</span></span>
