---
title: التبديل السلس دون اتصال لعمليات بطاقة الهدايا وإشعار الدائن
description: يقدم هذا الموضوع نظرة عامه حول التحسينات التي توفر تبديلا سلسا دون اتصال لأنواع دفع معينه.
author: rubendel
ms.date: 02/11/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.custom: 141393
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 20120-02-28
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 47867447e6d16a0fb4542c17ab184068300b2c1c
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/11/2021
ms.locfileid: "6019947"
---
# <a name="seamless-offline-switch-for-gift-card-and-credit-memo-operations"></a><span data-ttu-id="9f147-103">التبديل السلس دون اتصال لعمليات بطاقة الهدايا وإشعار الدائن</span><span class="sxs-lookup"><span data-stu-id="9f147-103">Seamless offline switch for gift card and credit memo operations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9f147-104">إذا كان هناك جهاز نقطه بيع (POS) يفقد اتصاله بقاعدة بيانات القناة، فيمكن متابعه معظم عمليات نقطه البيع والحركات التي كانت قيد التقدم بعد استلام الصراف رسالة تحذير حول فقد الاتصال.</span><span class="sxs-lookup"><span data-stu-id="9f147-104">If a point of sale (POS) device loses its connection to the channel database, most POS operations and transactions that were in progress can proceed after the cashier receives a warning message about the loss of connectivity.</span></span> <span data-ttu-id="9f147-105">ومع ذلك، في بعض الحالات، يكون للحركات عناصر تعتمد على الخدمة في الوقت الحقيقي، ولا يتم دعم هذه العناصر عندما تكون نقطة البيع دون اتصال.</span><span class="sxs-lookup"><span data-stu-id="9f147-105">However, in some cases, transactions have elements that rely on the real-time service, and those elements aren't supported when the POS is offline.</span></span> <span data-ttu-id="9f147-106">يصف هذا الموضوع بعض الوظائف التي تساعد علي تقليل تأثير الاتصال المفقود في هذه السيناريوهات.</span><span class="sxs-lookup"><span data-stu-id="9f147-106">This topic describes some functionality that helps reduce the impact of lost connectivity in these scenarios.</span></span>

## <a name="completing-gift-card-transactions-in-offline-mode"></a><span data-ttu-id="9f147-107">إكمال حركات بطاقات الهدايا في وضع دون الاتصال</span><span class="sxs-lookup"><span data-stu-id="9f147-107">Completing gift card transactions in offline mode</span></span>

<span data-ttu-id="9f147-108">تعتمد بطاقات الهدايا الداخلية على خدمة الوقت الفعلي، وذلك لأنه يجب الاحتفاظ بالرصيد الخاص ببطاقات الهدايا بشكل مركزي في المركز الرئيسي لـ Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="9f147-108">Internal gift cards depend on the real-time service, because the balance for the gift cards must be centrally maintained in Microsoft Dynamics 365 Commerce Headquarters.</span></span> <span data-ttu-id="9f147-109">للمساعدة في منع الاحتيال أو أية مشاكل أخرى في المزامنة، يتم تأمين بطاقات الهدايا بمجرد إضافتها إلى إحدى الحركات.</span><span class="sxs-lookup"><span data-stu-id="9f147-109">To help prevent fraud or other synchronization issues, gift cards are locked as soon as they are added to a transaction.</span></span> <span data-ttu-id="9f147-110">تضمن وظيفة التأمين عدم إمكانية استخدام بطاقة الهدايا في العديد من الوحدات الطرفية في نفس الوقت.</span><span class="sxs-lookup"><span data-stu-id="9f147-110">The locking function ensures that a gift card can't be used on multiple terminals at the same time.</span></span> <span data-ttu-id="9f147-111">عند اكتمال الحركة، يتم تحديث وتأمين بطاقة الهدايا تلقائيًا.</span><span class="sxs-lookup"><span data-stu-id="9f147-111">When a transaction is completed, the gift card is updated and unlocked.</span></span>

<span data-ttu-id="9f147-112">ومع ذلك، إذا فقدت نقطة البيع الاتصال بعد إضافة بطاقة الهدايا إلى حركة، فقد تصبح بطاقة الهدايا غير قابله للاستخدام.</span><span class="sxs-lookup"><span data-stu-id="9f147-112">However, if the POS loses connectivity after a gift card has been added to a transaction, the gift card can become unusable.</span></span> <span data-ttu-id="9f147-113">وللمساعدة في منع حدوث هذا الأمر، تم تزويد Dynamics 365 Commerce بمعلمة تتيح الحركات التي تشتمل على سطر بطاقة الهدايا يتم إكمالها عندما تكون نقطه البيع دون اتصال.</span><span class="sxs-lookup"><span data-stu-id="9f147-113">To help prevent this situation, Dynamics 365 Commerce has a parameter that enables transactions that include a gift card line to be completed while the POS is offline.</span></span> <span data-ttu-id="9f147-114">عند تشغيل هذه المعلمة، سيتم حفظ حركات بطاقة الهدايا التي تم فرضها دون اتصال مع الحركات غير المتصلة، وستتم مزامنتها في Commerce Headquarters عند مزامنة الحركات دون اتصال.</span><span class="sxs-lookup"><span data-stu-id="9f147-114">When this parameter is turned on, gift card transactions that are forced offline will be saved together with offline transactions, and they will be synced to Commerce Headquarters when the offline transactions are synced.</span></span> <span data-ttu-id="9f147-115">ستؤدي المزامنة أيضا إلى إلغاء تامين بطاقة الهدايا بحيث يمكن استخدامها في وحده طرفيه أخرى.</span><span class="sxs-lookup"><span data-stu-id="9f147-115">The synchronization will also unlock the gift card so that it can be used at another terminal.</span></span>

<span data-ttu-id="9f147-116">لتمكين الوظيفة بحيث تُكمل حركات بطاقة الهدايا بعد التبديل إلى وضع دون اتصال، انتقل إلى علامة التبويب **ترحيل** على صفحة **معلمات Commerce**.</span><span class="sxs-lookup"><span data-stu-id="9f147-116">To enable the functionality to conclude gift card transactions after switching to offline mode, go to the **Posting** tab on the **Commerce parameters** page.</span></span> <span data-ttu-id="9f147-117">في علامة التبويب هذه، حدد موقع علامة التبويب السريعة **بطاقة الهدايا** وقم بتعيين **‏‫السماح باختتام حركات بطاقات الهدايا في وضع دون الاتصال‬** إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="9f147-117">On that tab, locate the **Gift card** fasttab and set **Allow concluding gift card transactions in offline mode** to **Yes**.</span></span>

![إعداد بطاقة الهدايا بدون اتصال](../media/gift.png)

<span data-ttu-id="9f147-119">عادة ما يتم تخزين معلمات Commerce مؤقتا.</span><span class="sxs-lookup"><span data-stu-id="9f147-119">Commerce parameters are typically cached.</span></span> <span data-ttu-id="9f147-120">لذلك، بعد تحديث إعداد هذه المعلمة، وبدء قيام جدولة التوزيع بمزامنة التغيير إلى القناة، يمكن أن يستغرق التغيير 24 ساعة ليصبح ساري المفعول.</span><span class="sxs-lookup"><span data-stu-id="9f147-120">Therefore, after the setting of this parameter is updated, and the distribution schedule is initiated to sync the change to the channel, the change can take up to 24 hours to take effect.</span></span> <span data-ttu-id="9f147-121">لجعل التغيير فعالا على الفور، قم بإعادة تعيين Microsoft Internet Information Services (IIS).</span><span class="sxs-lookup"><span data-stu-id="9f147-121">To make the change effective immediately, reset Microsoft Internet Information Services (IIS).</span></span>

## <a name="completing-credit-memo-transactions-in-offline-mode"></a><span data-ttu-id="9f147-122">إكمال حركات إشعار دائن في وضع دون الاتصال</span><span class="sxs-lookup"><span data-stu-id="9f147-122">Completing credit memo transactions in offline mode</span></span>

<span data-ttu-id="9f147-123">على غرار بطاقات الهدايا الداخلية، يتم الاحتفاظ بإشعارات الدائن مركزيًا في Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="9f147-123">Like internal gift cards, credit memos are centrally maintained in Commerce Headquarters.</span></span> <span data-ttu-id="9f147-124">يحتوي Commerce على معلمه تتيح إكمال حركات إشعار الدائن عندما تكون نقطه البيع غير متصلة.</span><span class="sxs-lookup"><span data-stu-id="9f147-124">Commerce has a parameter that enables credit memo transactions to be completed while the POS is offline.</span></span> <span data-ttu-id="9f147-125">تعمل هذه المعلمة كمعلمه بطاقة الهدايا التي تم ذكرها في القسم السابق.</span><span class="sxs-lookup"><span data-stu-id="9f147-125">This parameter works like the gift card parameter that was mentioned in the previous section.</span></span> <span data-ttu-id="9f147-126">عند تشغيل المعلمة، ستتم إعادة مزامنة حركات إشعار الدائن التي تم فرضها دون اتصال إلى قاعدة بيانات القناة، مع الحركات الأخرى التي تم اجراؤها أثناء عدم اتصال نقطه البيع.</span><span class="sxs-lookup"><span data-stu-id="9f147-126">When the parameter is turned on, credit memo transactions that are forced offline will be synced back to the channel database, together with other transactions that were performed while the POS was offline.</span></span>

<span data-ttu-id="9f147-127">لتمكين الوظيفة بحيث تُكمل حركات إشعارات الدائن بعد التبديل إلى وضع دون اتصال، انتقل إلى علامة التبويب **ترحيل** على صفحة **معلمات Commerce**.</span><span class="sxs-lookup"><span data-stu-id="9f147-127">To enable the functionality to conclude credit memo transactions after switching to offline mode, go to the **Posting** tab on the **Commerce parameters** page.</span></span> <span data-ttu-id="9f147-128">في علامة التبويب هذه، حدد موقع علامة التبويب السريعة **إشعار دائن** وقم بتعيين **‏‫‏‫السماح باختتام حركات إشعارات الدائن في وضع دون الاتصال‬** إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="9f147-128">On that tab, locate the **Credit memo** fasttab and set **Allow concluding credit memo transactions in offline mode** to **Yes**.</span></span>

![إعداد إشعار الدائن دون اتصال](../media/creditmemo.png)

<span data-ttu-id="9f147-130">عادة ما يتم تخزين معلمات Commerce مؤقتا.</span><span class="sxs-lookup"><span data-stu-id="9f147-130">Commerce parameters are typically cached.</span></span> <span data-ttu-id="9f147-131">لذلك، بعد تحديث إعداد هذه المعلمة، وبدء قيام جدولة التوزيع بمزامنة التغيير إلى القناة، يمكن أن يستغرق التغيير 24 ساعة ليصبح ساري المفعول.</span><span class="sxs-lookup"><span data-stu-id="9f147-131">Therefore, after the setting of this parameter is updated, and the distribution schedule is initiated to sync the change to the channel, the change can take up to 24 hours to take effect.</span></span> <span data-ttu-id="9f147-132">لجعل التغيير فعالاً في الحال، قم بإعادة تعيين IIS.</span><span class="sxs-lookup"><span data-stu-id="9f147-132">To make the change effective immediately, reset IIS.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9f147-133">مواضيع مرتبطة</span><span class="sxs-lookup"><span data-stu-id="9f147-133">Related topics</span></span>

- [<span data-ttu-id="9f147-134">وظيفة نقطة البيع دون اتصال</span><span class="sxs-lookup"><span data-stu-id="9f147-134">Offline point of sale (POS) functionality</span></span>](../pos-offline-functionality.md)
- [<span data-ttu-id="9f147-135">عمليات نقاط البيع (POS) أثناء الاتصال وعدم الاتصال بالإنترنت</span><span class="sxs-lookup"><span data-stu-id="9f147-135">Online and offline point of sale (POS) operations</span></span>](../pos-operations.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]