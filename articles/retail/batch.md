---
title: معالجة محسنة للأصناف المتعقبة بطريقة دُفعية
description: يصف هذا الموضوع التحسينات التي تم إدخالها على معالجة الدُفعات للأصناف المتعقبة بطريقة دُفعية أثناء عملية ترحيل كشوف حسابات البيع بالتجزئة.
author: josaw1
manager: AnnBe
ms.date: 10/14/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-05-28
ms.dyn365.ops.version: 10
ms.openlocfilehash: 70d78f86f1df057d14d821a8c967e62eeeb4ff92
ms.sourcegitcommit: 0262a19e32b2c0c84c731d9f4fbe8ba91822afa3
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/15/2019
ms.locfileid: "2622540"
---
# <a name="improved-handling-of-batch-tracked-items"></a><span data-ttu-id="7c718-103">معالجة محسنة للأصناف المتعقبة بطريقة دُفعية</span><span class="sxs-lookup"><span data-stu-id="7c718-103">Improved handling of batch-tracked items</span></span>


[!include [banner](includes/banner.md)]

[!include [banner](includes/preview-banner.md)]


<span data-ttu-id="7c718-104">في نقطة البيع (POS) بالتجزئة، لا يمكن تسجيل أرقام الدُفعات للأصناف المتعقبة بطريقة دُفعية عند البيع.</span><span class="sxs-lookup"><span data-stu-id="7c718-104">In Retail Point of Sale (POS), batch numbers can't be captured for batch-tracked items at the time of sale.</span></span> <span data-ttu-id="7c718-105">ولكن فيما يتعلق بتكوينات محددة، عند ترحيل المبيعات إلى المقر الرئيسي عبر أوامر العميل أو ترحيل كشوف الحسابات، يتوقع نظام Microsoft Dynamics وجود أرقام دُفعات صالحة للأصناف المتعقبة بطريقة دُفعية، وأنها ستُستخدم خلال عملية الفوترة.</span><span class="sxs-lookup"><span data-stu-id="7c718-105">However, for specific configurations, when sales are posted in the headquarters through customer orders or statement posting, the Microsoft Dynamics system expects that valid batch numbers for batch-tracked items exist, and that they will be used during the invoicing process.</span></span>

<span data-ttu-id="7c718-106">إذا توفرت أرقام دُفعات صالحة للمنتجات، فستستخدمها عملية فوترة أوامر العميل وعملية فوترة أوامر المبيعات من ترحيل كشوف الحسابات.</span><span class="sxs-lookup"><span data-stu-id="7c718-106">If valid batch numbers are available for products, the customer order invoicing process and the sales order invoicing process from statement posting use them.</span></span> <span data-ttu-id="7c718-107">وبخلاف ذلك، لا يمكن ترحيل عملية فوترة أوامر العميل، ويتلقى مستخدم نقطة البيع رسالة خطأ.</span><span class="sxs-lookup"><span data-stu-id="7c718-107">Otherwise, the customer order invoicing process can't post, and the POS user receives an error message.</span></span> <span data-ttu-id="7c718-108">بعد ذلك، تدخل عملية ترحيل كشوف الحسابات في حالة الخطأ.</span><span class="sxs-lookup"><span data-stu-id="7c718-108">Statement posting then goes into an error state.</span></span> <span data-ttu-id="7c718-109">تحدث حالة الخطأ هذه حتى عند تشغيل مخزون سالب للمنتجات.</span><span class="sxs-lookup"><span data-stu-id="7c718-109">This error state occurs even when negative inventory has been turned on for the products.</span></span>

<span data-ttu-id="7c718-110">بإمكان التحسينات التي تم إدخالها على إصدار البيع بالتجزئة 10.0.4l والإصدارات اللاحقة المساعدة في ضمان عدم حظر فوترة طلب العميل وفوترة أوامر المبيعات عبر ترحيل كشوف الحسابات لهذه الأصناف إذا كانت قيمة المخزون 0 (صفر) أو إذا كان رقم دُفعة ما غير متوفر، وذلك عند تشغيل المخزون السالب للأصناف المتعقبة بطريقة دُفعية.</span><span class="sxs-lookup"><span data-stu-id="7c718-110">Improvements that have been made in Retail version 10.0.4 and later help guarantee that, when negative inventory is turned on for batch-tracked items, customer order invoicing and sales order invoicing through statement posting aren't blocked for those items if the inventory is 0 (zero) or a batch number isn't available.</span></span> <span data-ttu-id="7c718-111">تستخدم الوظيفة الجديدة معرف الدُفعة الافتراضي لبنود المبيعات عندما لا تتوفر أرقام الدُفعات.</span><span class="sxs-lookup"><span data-stu-id="7c718-111">The new functionality uses a default batch ID for the sales lines when batch numbers aren't available.</span></span>

<span data-ttu-id="7c718-112">لتحديد معرف الدُفعة الافتراضي المستخدم لأوامر العميل، في صفحة **معلمات البيع بالتجزئة**، على علامة تبويب **أوامر العميل**، على علامة التبويب السريعة **الأمر**، قم بتعيين حقل **معرف الدُفعة الافتراضي**.</span><span class="sxs-lookup"><span data-stu-id="7c718-112">To define the default batch ID that is used for customer orders, on the **Retail parameters** page, on the **Customer orders** tab, on the **Order** FastTab, set the **Default batch id** field.</span></span>

<span data-ttu-id="7c718-113">لتحديد معرف الدُفعة الافتراضي المستخدم لفوترة أوامر المبيعات من خلال ترحيل كشوف الحسابات، في صفحة **معلمات البيع بالتجزئة**، على علامة تبويب **ترحيل**، على علامة التبويب السريعة **تحديث المخزون**، قم بتعيين حقل **معرف الدُفعة الافتراضي**.</span><span class="sxs-lookup"><span data-stu-id="7c718-113">To define the default batch ID that is used for sales order invoicing through statement posting, on the **Retail parameters** page, on the **Posting** tab, on the **Inventory update** FastTab, set the **Default batch id** field.</span></span>

> [!NOTE]
> <span data-ttu-id="7c718-114">تتوفر هذه الوظيفة فقط عند تشغيل التخزين المتقدم في المستودع للمستودع المعين والأصناف المعينة.</span><span class="sxs-lookup"><span data-stu-id="7c718-114">This functionality is available only when advanced warehousing is turned on for the specific store warehouse and items.</span></span> <span data-ttu-id="7c718-115">في إصدار لاحق، سيتم دعم الوظيفة أيضًا للسيناريوهات التي لا يتم فيها استخدام إدارة المستودعات المتقدمة.</span><span class="sxs-lookup"><span data-stu-id="7c718-115">In a later release, the functionality will also be supported for scenarios where advanced warehouse management isn't used.</span></span>

> [!NOTE]
> <span data-ttu-id="7c718-116">دعم المعالجة المحسنة للأصناف المتعقبة بطريقة دُفعية‬ أثناء ترحيل كشف الحساب لسيناريوهات إدارة المستودعات غير المتقدمة التي تم تقديمها في الإصدار 10.0.5 من Retail.</span><span class="sxs-lookup"><span data-stu-id="7c718-116">Support for improved handling of batch-tracked items during statement posting for non-advanced warehouse management scenarios was introduced in Retail version 10.0.5.</span></span>
