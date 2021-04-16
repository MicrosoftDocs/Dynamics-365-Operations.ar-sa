---
title: الأوصاف الافتراضية لدفتر الأستاذ العام
description: يمكن استخدام الأوصاف الافتراضية لتحديث حقل الوصف في ترحيلات الإيصالات إلى دفتر الأستاذ العام.
author: sherry-zheng
ms.date: 12/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TransactionTexts
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-07
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: d5a38af57d614ae2c93b0af74ec4a1c085519d46
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/01/2021
ms.locfileid: "5841877"
---
# <a name="default-descriptions-for-the-general-ledger"></a><span data-ttu-id="ab818-103">الأوصاف الافتراضية لدفتر الأستاذ العام</span><span class="sxs-lookup"><span data-stu-id="ab818-103">Default descriptions for the general ledger</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ab818-104">يمكن استخدام الأوصاف الافتراضية لتحديث حقل **الوصف** في ترحيلات الإيصالات إلى دفتر الأستاذ العام.</span><span class="sxs-lookup"><span data-stu-id="ab818-104">Default descriptions can be used to update the **Description** field in voucher postings to the general ledger.</span></span> <span data-ttu-id="ab818-105">تم تحسين هذه الوظيفة للعمل مع التكلفة شاملة التفريغ.</span><span class="sxs-lookup"><span data-stu-id="ab818-105">This functionality has been enhanced to work with Landed cost.</span></span>

<span data-ttu-id="ab818-106">لإعداد الأوصاف الافتراضية لترحيلات دفتر الأستاذ، انتقل إلى **الإدارة التنظيمية \> الإعداد \> الأوصاف الافتراضية**.</span><span class="sxs-lookup"><span data-stu-id="ab818-106">To set up default descriptions for ledger postings, go to **Organizational administration \> Setup \> Default descriptions**.</span></span>

<span data-ttu-id="ab818-107">يسرد الجدول التالي القيم الجديدة التي تمت إضافتها للحقل **الوصف** في صفحة **الأوصاف الافتراضية** لدعم التكلفة شاملة التفريغ.</span><span class="sxs-lookup"><span data-stu-id="ab818-107">The following table lists the new values that have been added for the **Description** field on the **Default descriptions** page to support Landed cost.</span></span>

| <span data-ttu-id="ab818-108">نوع الوصف</span><span class="sxs-lookup"><span data-stu-id="ab818-108">Description type</span></span> | <span data-ttu-id="ab818-109">الملاحظات</span><span class="sxs-lookup"><span data-stu-id="ab818-109">Notes</span></span> |
|---|---|
| <span data-ttu-id="ab818-110">تكاليف الاستيراد - استحقاق التكلفة</span><span class="sxs-lookup"><span data-stu-id="ab818-110">Import costing – Cost accrual</span></span> | <span data-ttu-id="ab818-111">عند ترحيل فاتورة أمر شراء، تتم معالجة استحقاق التكلفة لتقدير تكاليف الرحلة.</span><span class="sxs-lookup"><span data-stu-id="ab818-111">When a purchase order invoice is posted, a cost accrual is processed for estimate voyage costs.</span></span> <span data-ttu-id="ab818-112">يمكن تحديد الأوصاف الافتراضية لإضافة رقم الرحلة إلى الوصف.</span><span class="sxs-lookup"><span data-stu-id="ab818-112">Default descriptions can be specified to add the voyage number to the description.</span></span> <span data-ttu-id="ab818-113">استخدم *%4* لرقم الشحنة.</span><span class="sxs-lookup"><span data-stu-id="ab818-113">Use *%4* for the shipment number.</span></span> |
| <span data-ttu-id="ab818-114">تكاليف الاستيراد - أمر بضاعة بالطريق</span><span class="sxs-lookup"><span data-stu-id="ab818-114">Import costing – Goods in transit order</span></span> | <span data-ttu-id="ab818-115">إذا كنت تستخدم معالجة الإرسال النقل، سيتم ترحيل فاتورة أمر الشراء، وترحيل البضائع إلى بضائع في حساب البضاعة بالطريق.</span><span class="sxs-lookup"><span data-stu-id="ab818-115">If you're using in-transit processing, the purchase order invoice is posted, and the goods are posted to a goods in transit account.</span></span> <span data-ttu-id="ab818-116">يمكن تحديد الأوصاف الافتراضية لإضافة رقم أمر النقل إلى الوصف.</span><span class="sxs-lookup"><span data-stu-id="ab818-116">Default descriptions can be specified to add the in-transit order number to the description.</span></span> <span data-ttu-id="ab818-117">تستخدم *%4* لرقم أمر النقل.</span><span class="sxs-lookup"><span data-stu-id="ab818-117">Use *%4* for the in-transit order number.</span></span> |
| <span data-ttu-id="ab818-118">المخزون - إقفال - تسوية</span><span class="sxs-lookup"><span data-stu-id="ab818-118">Inventory – close – adjustment</span></span> | <span data-ttu-id="ab818-119">عند معالجة فاتورة الحسابات الدائنة (AP) لتكلفه الرحلة، تتم معالجة تسوية المخزون لتقدير تكاليف الرحلة.</span><span class="sxs-lookup"><span data-stu-id="ab818-119">When the accounts payable (AP) invoice is processed for a voyage cost, an inventory adjustment is processed to estimate voyage costs.</span></span> <span data-ttu-id="ab818-120">يمكن تحديد الأوصاف الافتراضية لإضافة رقم الرحلة إلى الوصف.</span><span class="sxs-lookup"><span data-stu-id="ab818-120">Default descriptions can be specified to add the voyage number to the description.</span></span> <span data-ttu-id="ab818-121">استخدم *%4* لرقم الشحنة.</span><span class="sxs-lookup"><span data-stu-id="ab818-121">Use *%4* for the shipment number.</span></span> |

<span data-ttu-id="ab818-122">لمزيد من المعلومات حول كيفيه العمل مع صفحة **‏‫الأوصاف الافتراضية** ، راجع [اعداد الأوصاف الافتراضية للترحيل التلقائي](../../finance/general-ledger/set-up-default-descriptions-for-automatic-posting.md).</span><span class="sxs-lookup"><span data-stu-id="ab818-122">For more information about how to work with the **Default descriptions** page, see [Set up default descriptions for automatic posting](../../finance/general-ledger/set-up-default-descriptions-for-automatic-posting.md).</span></span>
