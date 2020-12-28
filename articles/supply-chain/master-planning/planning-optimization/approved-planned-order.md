---
title: الموافقة على أوامر مخططة
description: يصف هذا الموضوع الموافقة على الأوامر المخططة المدعومة في تحسين التخطيط‬.
author: ChristianRytt
manager: tfehr
ms.date: 08/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-08-21
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: b7975088be898ccecceb1f7be009cecff107f6e6
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/13/2020
ms.locfileid: "4421341"
---
# <a name="approve-planned-orders"></a><span data-ttu-id="0c4f4-103">الموافقة على أوامر مخططة</span><span class="sxs-lookup"><span data-stu-id="0c4f4-103">Approve planned orders</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0c4f4-104">يوفر هذا الموضوع معلومات حول كيفية تحديث حالة الأوامر المخططة في تحسين التخطيط.</span><span class="sxs-lookup"><span data-stu-id="0c4f4-104">This topic provides information about how to update the status of planned orders in Planning Optimization.</span></span>

<span data-ttu-id="0c4f4-105">لاحظ أن الموافقة على الأوامر المخططة هي خطوة اختيارية نحو إنشاء أمر مؤكد من أمر مخطط.</span><span class="sxs-lookup"><span data-stu-id="0c4f4-105">Note that approval of planned orders is an optional step, on the way to create a firmed order from a planned order.</span></span> <span data-ttu-id="0c4f4-106">من المستحسن الموافقة على الأوامر المخططة المعدلة، وإلا فسيتم تجاهل عمليات التحرير وستتم الكتابة فوقها في عملية تشغيل التخطيط التالية.</span><span class="sxs-lookup"><span data-stu-id="0c4f4-106">It is recommended to approve modified planned orders, otherwise the edits will be ignored and overwritten by the next planning run.</span></span>

![سير مهام الأمر المخطط](media/approved-planned-orders-1.png)

<span data-ttu-id="0c4f4-108">يساعدك حقل **الحالة** في تعقب تقدمك باستخدام القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="0c4f4-108">The **Status** field helps you tack your progress using the following values:</span></span>

- <span data-ttu-id="0c4f4-109">**غير معالج:** عندما يُنشئ التخطيط الرئيسي أوامر مخططة، تكون حالة الأوامر المخططة *غير معالج*.</span><span class="sxs-lookup"><span data-stu-id="0c4f4-109">**Unprocessed:** When master planning generates planned orders, the planned orders have a status of *Unprocessed*.</span></span> <span data-ttu-id="0c4f4-110">سيتم حذف الأوامر المخططة بهذه الحالة اثناء عملية تشغيل التخطيط التالية.</span><span class="sxs-lookup"><span data-stu-id="0c4f4-110">Planned orders with this status will be deleted during the next planning run.</span></span>
- <span data-ttu-id="0c4f4-111">**مكتمل:** إذا قررت عدم تأكيد أمر مخطط،يمكنك تغيير الحالة إلى *مكتمل* للإشارة إلى إكمال تقييم هذا الأمر المخطط.</span><span class="sxs-lookup"><span data-stu-id="0c4f4-111">**Completed:** If you decide not to firm a planned order, you can change the status to *Completed* to indicate that you completed evaluating this planned order.</span></span> <span data-ttu-id="0c4f4-112">لاحظ أن التعامل مع حالة أمر *غير معالج* وأمر *مكتمل* بالطريقة نفسها من قبل النظام.</span><span class="sxs-lookup"><span data-stu-id="0c4f4-112">Note that a status of *Unprocessed* and *Completed* are treated the same by the system.</span></span>
- <span data-ttu-id="0c4f4-113">**موافق عليه‬‬:** إذا أردت الاحتفاظ بعمليات التحرير أو كنت تخطط لتأكيد أمر مخطط، فعليك تغيير الحالة إلى *موافق عليه‬‬*.</span><span class="sxs-lookup"><span data-stu-id="0c4f4-113">**Approved:** If you want to keep edits or are planning to firm a planned order, change the status to *Approved*.</span></span> <span data-ttu-id="0c4f4-114">تُعتبر الأوامر المُخططة التي لها حالة *موافق عليه* بمثابة توريد ثابت ومتوقع من قبل التخطيط الرئيسي، بحيث لا يتم تعديلها أو حذفها أثناء عملية تشغيل لاحقة للتخطيط الرئيسي.</span><span class="sxs-lookup"><span data-stu-id="0c4f4-114">Planned orders with *Approved* status are considered as fixed and expected supply by master planning, so they are not modified or deleted during later master planning runs.</span></span> <span data-ttu-id="0c4f4-115">لتحقيق هذا، ينسخ منطق التخطيط الأوامر المخططة *المعتمدة* من إصدار الخطة القديمة إلى إصدار الخطة الجديدة أثناء التخطيط الرئيسي.</span><span class="sxs-lookup"><span data-stu-id="0c4f4-115">To achieve this, the planning logic copies the *Approved* planned orders from the old plan version to the new plan version during master planning.</span></span> <span data-ttu-id="0c4f4-116">لاحظ أن الأمر المخطط بالحالة *موافق عليه* يعتبر بمثابة توريد فقط ضمن الخطة الرئيسية المحددة.</span><span class="sxs-lookup"><span data-stu-id="0c4f4-116">Note that *Approved* planned orders are only considered supply within the specific master plan.</span></span>

<span data-ttu-id="0c4f4-117">يمكنك إدارة الأوامر المخططة من مساحة عمل **التخطيط الرئيسي**، أو قائمة **الأمر المخطط**، أو قوائم **أوامر الإنتاج المخططة**، و **أوامر الشراء المخططة**، و **التحويل المخطط**.</span><span class="sxs-lookup"><span data-stu-id="0c4f4-117">You can manage planned orders from the  **Master planning**  workspace, the  **Planned order**  list, or the  **Planned production orders**,  **Planned purchase orders**, and  **Planned transfer**  lists.</span></span>
