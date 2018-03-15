---
title: "تأكيد المنتج لانتقاء نظام المجموعة"
description: "يصف هذا الموضوع كيفية إعداد خاصية التحقق من الصنف إلى جانب انتقاء نظام المجموعة."
author: Mirzaab
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSRFAutoConfirm
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a1c4b7623f3409d4474adcd04fb1331b944b9fbb
ms.openlocfilehash: 530082a23163cf348bcbb133175e3af963d55f2b
ms.contentlocale: ar-sa
ms.lasthandoff: 02/13/2018

---

[!include[banner](../includes/banner.md)]

# <a name="product-confirmation-for-cluster-picking"></a><span data-ttu-id="ec64e-103">تأكيد المنتج لانتقاء نظام المجموعة</span><span class="sxs-lookup"><span data-stu-id="ec64e-103">Product confirmation for cluster picking</span></span>
<span data-ttu-id="ec64e-104">يسمح لك انتقاء نظام المجموعة بانتقاء الأصناف لأوامر متعددة في نفس الوقت.</span><span class="sxs-lookup"><span data-stu-id="ec64e-104">Cluster picking allows you to pick items for several orders at the same time.</span></span> <span data-ttu-id="ec64e-105">عند تطبيق انتقاء نظام المجموعة، يُعد تأكيد الصنف أمرًا هامًا للتحقق من الأصناف التي تمت إضافتها إلى نظم المجموعات.</span><span class="sxs-lookup"><span data-stu-id="ec64e-105">When cluster picking is applied, item confirmation is crucial to verify the items that are added to clusters.</span></span> <span data-ttu-id="ec64e-106">يمكنك التحقق من الأصناف في انتقاء نظام المجموعة خلال عملية انتقاء نظام المجموعة.</span><span class="sxs-lookup"><span data-stu-id="ec64e-106">You can verify items in cluster picking during the cluster picking process.</span></span>

## <a name="where-it-applies"></a><span data-ttu-id="ec64e-107">أين يتم التطبيق</span><span class="sxs-lookup"><span data-stu-id="ec64e-107">Where it applies</span></span>
<span data-ttu-id="ec64e-108">يعمل التحقق من صحة الصنف لانتقاء نظام المجموعة على النحو نفسه عندما تقوم بالتحقق من الأصناف في عمليات انتقاء النظم غير المجمعة.</span><span class="sxs-lookup"><span data-stu-id="ec64e-108">Item verification for cluster picking works the same way as when you verify items in a non-cluster picking processes.</span></span> <span data-ttu-id="ec64e-109">يستند الإعداد على إعداد الرمز الشريطي للمنتج.</span><span class="sxs-lookup"><span data-stu-id="ec64e-109">The setup is based on the product bar code setup.</span></span>

## <a name="set-up-item-verification-with-cluster-picking"></a><span data-ttu-id="ec64e-110">إعداد التحقق من الصنف مع انتقاء نظام مجموعة</span><span class="sxs-lookup"><span data-stu-id="ec64e-110">Set up item verification with cluster picking</span></span>
1.  <span data-ttu-id="ec64e-111">في عنصر قائمة جهاز محمول، قم بفتح نموذج إعداد لتأكيد العمل: **إدارة المستودعات** > **إدارة المستودعات** > **الإعداد** > **جهاز محمول** > **عناصر قائمة الجهاز المحمول**.</span><span class="sxs-lookup"><span data-stu-id="ec64e-111">On a mobile device menu item, open the setup form for work confirmation: **Warehouse management** > **Warehouse management** > **Setup** > **Mobile device** > **Mobile device menu items**.</span></span>
2.  <span data-ttu-id="ec64e-112">من عنصر قائمة الجهاز المحمول، قم بفتح **إعداد تأكيد العمل**.</span><span class="sxs-lookup"><span data-stu-id="ec64e-112">From the mobile device menu item, open **Work confirmation setup**.</span></span>

| <span data-ttu-id="ec64e-113">الخيار</span><span class="sxs-lookup"><span data-stu-id="ec64e-113">Option</span></span>        | <span data-ttu-id="ec64e-114">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="ec64e-114">Description</span></span>   | 
| ------------- | ------------- |
|<span data-ttu-id="ec64e-115">تأكيد المنتج</span><span class="sxs-lookup"><span data-stu-id="ec64e-115">Product confirmation</span></span> | <span data-ttu-id="ec64e-116">يسمح لك بالتحقق من كل جزء من المخزون من خلال الهاتف المحمول عند مسحه ضوئيًا.</span><span class="sxs-lookup"><span data-stu-id="ec64e-116">Allows you to verify each piece of inventory from the mobile device when scanned.</span></span>|

