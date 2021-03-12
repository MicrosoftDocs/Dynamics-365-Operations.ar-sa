---
title: تسلسل التكلفة الاحتياطية للمتوسط المتحرك
description: يوفر هذا الموضوع معلومات حول تسلسلات التكاليف الاحتياطية الخاصة بحسابات المتوسط المتحرك في Microsoft Dynamics 365 Supply Chain Management.
author: AndersGirke
manager: tfehr
ms.date: 03/25/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2020-03-25
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: 541b7ecca5c1c36999f573d6d0f2dc0c9e901631
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "4967573"
---
# <a name="moving-average-fallback-cost-sequence"></a><span data-ttu-id="dae60-103">تسلسل التكلفة الاحتياطية للمتوسط المتحرك</span><span class="sxs-lookup"><span data-stu-id="dae60-103">Moving average fallback cost sequence</span></span>

<span data-ttu-id="dae60-104">هناك طريقة لحساب تكلفة المخزون وهي استخدام _متوسط متحرك_.</span><span class="sxs-lookup"><span data-stu-id="dae60-104">One way that you can calculate the cost of your inventory is by using a _moving average_.</span></span> <span data-ttu-id="dae60-105">يمكن إقران ثلاث قيم تكلفة كحدٍ أقصى بكل صنف من أصناف المخزون:</span><span class="sxs-lookup"><span data-stu-id="dae60-105">Up to three cost values can be associated with each inventory item:</span></span>

- <span data-ttu-id="dae60-106">**الإصدار الأخير** – تكلفة الإصدار الأخير الذي تم تعيينه قبل أن يصبح المخزون سالبًا</span><span class="sxs-lookup"><span data-stu-id="dae60-106">**Last issue** – The last issue cost that was assigned before inventory went negative</span></span>
- <span data-ttu-id="dae60-107">**التكلفة النشطة** – التكلفة الأخيرة التي تم تنشيطها في إصدار التكاليف</span><span class="sxs-lookup"><span data-stu-id="dae60-107">**Active cost** – The latest cost that was activated in a costing version</span></span>
- <span data-ttu-id="dae60-108">**سعر الصنف** – التكلفة المحددة للمنتج الصادر</span><span class="sxs-lookup"><span data-stu-id="dae60-108">**Item price** – The cost that is specified for the released product</span></span>

<span data-ttu-id="dae60-109">لتحديد أي قيمة من قيم التكلفة هذه يجب استخدامها في عمليات حسب المتوسط المتحرك، يستخدم النظام _تسلسل التكلفة الاحتياطية_ لإنشاء ترتيب تفضيلات للقيم.</span><span class="sxs-lookup"><span data-stu-id="dae60-109">To determine which of these cost values should be used in moving average calculations, the system uses a _fallback cost sequence_ to establish the order of preference for the values.</span></span> <span data-ttu-id="dae60-110">إذا لم تكن قيمة التكلفة المفضلة متاحة، فإن النظام يستخدم القيمة المفضلة التالية، وهكذا.</span><span class="sxs-lookup"><span data-stu-id="dae60-110">If the preferred cost value isn't available, the system uses the next-preferred value, and so on.</span></span>

<span data-ttu-id="dae60-111">في الإصدارات السابقة من Microsoft Dynamics 365 Supply Chain Management، استخدم النظام تسلسل تكلفة احتياطية ثابتة (_الإصدار الأخير – التكلفة النشطة – سعر الصنف_).</span><span class="sxs-lookup"><span data-stu-id="dae60-111">In previous versions of Microsoft Dynamics 365 Supply Chain Management, the system used a fixed fallback cost sequence (_Last issue – Active cost – Item price_).</span></span> <span data-ttu-id="dae60-112">هذا التسلسل لا يزال التسلسل الافتراضي في الإصدار 10.0.11.</span><span class="sxs-lookup"><span data-stu-id="dae60-112">In version 10.0.11, this sequence is still the default sequence.</span></span> <span data-ttu-id="dae60-113">ومع ذلك، يمكنك أيضًا تشغيل ميزة تسمح لك بالتحديد من بين ثلاثة تسلسلات تكلفة احتياطية متاحة.</span><span class="sxs-lookup"><span data-stu-id="dae60-113">However, you can also turn on a feature that lets you select among three available fallback cost sequences.</span></span> <span data-ttu-id="dae60-114">بإمكان هذه الميزة أن تكون مفيدة بشكل خاص للمؤسسات التي تستخدم قيم المخزون السالب بانتظام.</span><span class="sxs-lookup"><span data-stu-id="dae60-114">This feature can be especially useful for organizations that regularly use negative inventory values.</span></span>

<span data-ttu-id="dae60-115">لجعل محدد تسلسل التكلفة الاحتياطية متوفرًا، يجب عليك أنت (أو المسؤول) استخدام [إدارة الميزات](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) لتشغيل ميزة مسماة _تسلسل التكلفة الاحتياطية للمتوسط المتحرك_.</span><span class="sxs-lookup"><span data-stu-id="dae60-115">To make the selector for the fallback cost sequence available, you (or an admin) must use [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) to turn on the feature that is named _Moving average fallback cost sequence_.</span></span>

<span data-ttu-id="dae60-116">لتحديد تسلسل التكلفة الاحتياطية لعمليات حساب المتوسط المتحرك، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="dae60-116">To select the fallback cost sequence for moving average calculations, follow these steps.</span></span>

1. <span data-ttu-id="dae60-117">افتح صفحة **المعلمات**.</span><span class="sxs-lookup"><span data-stu-id="dae60-117">Open the **Parameters** page.</span></span>
2. <span data-ttu-id="dae60-118">على علامة تبويب **حساب المخزون**، في القسم **المتوسط المتحرك**، عيّن قيمة الحقل **تسلسل التكلفة الاحتياطية** إلى إحدى القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="dae60-118">On the **Inventory accounting** tab, in the **Moving average** section, set the **Fallback cost sequence** field to one of the following values:</span></span>

    - <span data-ttu-id="dae60-119">**الإصدار الأخير – التكلفة النشطة – سعر الصنف** – هذا التسلسل هو التسلسل الافتراضي.</span><span class="sxs-lookup"><span data-stu-id="dae60-119">**Last issue – Active cost – Item price** – This sequence is the default sequence.</span></span> <span data-ttu-id="dae60-120">إنه التسلسل نفسه المستخدم إذا لم تكن ميزة _تسلسل التكلفة الاحتياطية للمتوسط المتحرك‬_ قيد التشغيل.</span><span class="sxs-lookup"><span data-stu-id="dae60-120">It's the same sequence that is used if the _Moving average fallback cost sequence_ feature isn't turned on.</span></span>
    - <span data-ttu-id="dae60-121">**التكلفة النشطة - الإصدار الأخير**</span><span class="sxs-lookup"><span data-stu-id="dae60-121">**Active cost – Last issue**</span></span>
    - <span data-ttu-id="dae60-122">**التكلفة النشطة – سعر الصنف** – قد تواجه المؤسسات مشكلات في الأداء إذا كانت تستخدم عمليات الأعمال حيث المخزون يكون سالبًا بشكل منتظم، وحجم الحركات مرتفعًا في الوقت نفسه.</span><span class="sxs-lookup"><span data-stu-id="dae60-122">**Active cost – Item price** – Organizations might experience performance issues if they use business processes where inventory regularly goes negative and, at the same time, the transaction volume is high.</span></span> <span data-ttu-id="dae60-123">بإمكان هذا الإعداد أن يساعد على تخفيف مشكلات الأداء هذه.</span><span class="sxs-lookup"><span data-stu-id="dae60-123">This setting can help mitigate those performance issues.</span></span>

<span data-ttu-id="dae60-124">![معلمات محاسبة المخزون](media/inventory-accounting-parameters.png "معلمات محاسبة المخزون")</span><span class="sxs-lookup"><span data-stu-id="dae60-124">![Inventory accounting parameters](media/inventory-accounting-parameters.png "Inventory accounting parameters")</span></span>
