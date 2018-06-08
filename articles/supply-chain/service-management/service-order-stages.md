---
title: "مراحل أمر خدمة"
description: "من خلا تحديد مراحل لأمر الخدمة وتعيينها إلى العاملين، فإنك تتحكم في تدفق أمر الخدمة من خلال المهام التي ينفذها العديد من الأشخاص في مؤسسة الخدمة."
author: YuyuScheller
manager: AnnBe
ms.date: 04/30/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAServiceOrderTable, SMAStageTable
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
ms.openlocfilehash: 9aa90dfcfc4b30d6cb4fa7ed4e6faaf505548d41
ms.contentlocale: ar-sa
ms.lasthandoff: 05/08/2018

---

# <a name="service-order-stages"></a><span data-ttu-id="ad5a2-103">مراحل أمر خدمة</span><span class="sxs-lookup"><span data-stu-id="ad5a2-103">Service order stages</span></span>   

[!include [banner](../includes/banner.md)]


<span data-ttu-id="ad5a2-104">يمكنك إعداد مراحل أمر الخدمة لتحديد المهام التي يجب إكمالها والترتيب الذي يتم إكمالها به والعاملين المسؤولين عن الانتهاء منها.</span><span class="sxs-lookup"><span data-stu-id="ad5a2-104">You can set up stages for a service order to define the tasks that must be completed, the order in which they are completed, and the workers who are responsible for completing them.</span></span> <span data-ttu-id="ad5a2-105">بتحديد مراحل لأمر الخدمة وتعيينها إلى العاملين، يمكن التحكم في تدفق أمر الخدمة من خلال المهام التي ينفذها العديد من الأشخاص في مؤسسة الخدمة.</span><span class="sxs-lookup"><span data-stu-id="ad5a2-105">By defining the stages for a service order and assigning them to workers, you can control the flow of a service order through the tasks that various people perform in the service organization.</span></span> <span data-ttu-id="ad5a2-106">يجب أن يحتوي تسلسل المراحل على مرحلة أولية.</span><span class="sxs-lookup"><span data-stu-id="ad5a2-106">The sequence of stages must include an initial stage.</span></span>

<span data-ttu-id="ad5a2-107">يمكنك أيضا تعريف الإجراءات المسموح بها في كل مرحلة.</span><span class="sxs-lookup"><span data-stu-id="ad5a2-107">You can also define the actions that are permitted at each stage.</span></span> <span data-ttu-id="ad5a2-108">على سبيل المثال، إذا قمت بإلغاء تحديد خانة الاختيار **ترحيل** لجميع المراحل باستثناء المرحلة النهائية، فإنه يتم بذلك منع ترحيل أية أوامر خدمة قبل أن تتم معالجة أوامر الخدمة عبر تسلسل المراحل بأكمله.</span><span class="sxs-lookup"><span data-stu-id="ad5a2-108">For example, if you clear the **Post** check box for all stages except the final stage, you prevent any service orders from being posted before the service orders are processed through the complete sequence of stages.</span></span>

## <a name="branching-in-service-order-stages"></a><span data-ttu-id="ad5a2-109">التفريع في مراحل أمر الخدمة</span><span class="sxs-lookup"><span data-stu-id="ad5a2-109">Branching in service order stages</span></span>

<span data-ttu-id="ad5a2-110">عند إعداد مرحلة خدمة، يمكنك إنشاء خيارات متعددة أو فروع، للتحديد من بينها لمرحلة الخدمة التالية.</span><span class="sxs-lookup"><span data-stu-id="ad5a2-110">When you set up a service stage, you can create multiple options, or branches, to select from for the next service stage.</span></span> <span data-ttu-id="ad5a2-111">تتوفر كافة الفروع التي تقوم بإنشائها للاختيار من بينها عند اكتمال المرحلة الأولية.</span><span class="sxs-lookup"><span data-stu-id="ad5a2-111">All the branches that you create are available to select from when the initial stage is completed.</span></span> <span data-ttu-id="ad5a2-112">على سبيل المثال، يمكنك إعداد **التخطيط** كمرحلة أولية.</span><span class="sxs-lookup"><span data-stu-id="ad5a2-112">For example, you set up **Planning** as an initial stage.</span></span> <span data-ttu-id="ad5a2-113">يمكنك إنشاء مرحلتين تحملان الإسمين **قيد التنفيذ** و **إلغاء**، ثم تحديد **التخطيط** لتكون المرحلة الأصل الخاصة بهما.</span><span class="sxs-lookup"><span data-stu-id="ad5a2-113">You create two stages named **In process** and **Cancel**, and then select **Planning** as the parent for them.</span></span> <span data-ttu-id="ad5a2-114">قم بتعيين مرحلة **التخطيط** إلى أمر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="ad5a2-114">You assign the **Planning** stage to sales order.</span></span> <span data-ttu-id="ad5a2-115">عند اكتمال مرحلة التخطيط لأمر المبيعات، يمكنك تحديد مرحلة **قيد التنفيذ** إذا كان أمر المبيعات جاهز للعمل، أو يمكنك تحديد مرحلة **إلغاء** إذا تم إلغاء أمر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="ad5a2-115">When the planning stage for the sales order is completed, you can select the **In process** stage if the sales order is ready to work on, or you can select the **Cancel** stage if the sales order is canceled.</span></span>

## <a name="see-also"></a><span data-ttu-id="ad5a2-116">راجع أيضًا</span><span class="sxs-lookup"><span data-stu-id="ad5a2-116">See also</span></span>

[<span data-ttu-id="ad5a2-117">إعداد مراحل أمر الخدمة</span><span class="sxs-lookup"><span data-stu-id="ad5a2-117">Set up service order stages</span></span>](set-up-service-order-stages.md)

[<span data-ttu-id="ad5a2-118">تغيير مرحلة أمر الخدمة</span><span class="sxs-lookup"><span data-stu-id="ad5a2-118">Change the service order stage</span></span>](change-service-order-stage.md)

  


