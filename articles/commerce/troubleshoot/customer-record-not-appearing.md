---
title: لا تظهر سجلات العملاء في المركز الرئيسية لـ Commerce
description: يوفر هذا الموضوع إرشادات استكشاف الأخطاء وإصلاحها التي يمكن أن تساعد في حالة عدم ظهور سجلات العملاء على الفور في المركز الرئيسي لـ Commerce.
author: Reza-Assadi
manager: AnnBe
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 790468ac244f1647c07024604886c65d22feca24
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585176"
---
# <a name="customer-records-dont-appear-in-commerce-headquarters"></a><span data-ttu-id="861b4-103">لا تظهر سجلات العملاء في المركز الرئيسية لـ Commerce</span><span class="sxs-lookup"><span data-stu-id="861b4-103">Customer records don't appear in Commerce headquarters</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="861b4-104">يوفر هذا الموضوع إرشادات استكشاف الأخطاء وإصلاحها التي يمكن أن تساعد في حالة عدم ظهور سجلات العملاء على الفور في المركز الرئيسي لـ Commerce.</span><span class="sxs-lookup"><span data-stu-id="861b4-104">This topic provides troubleshooting guidance that can help when customer records don't immediately appear in Commerce headquarters.</span></span>

## <a name="description"></a><span data-ttu-id="861b4-105">الوصف</span><span class="sxs-lookup"><span data-stu-id="861b4-105">Description</span></span>

<span data-ttu-id="861b4-106">عند إنشاء سجل عميل جديد باستخدام تدفق التسجيل في واجهة متجر التجارة الإلكترونية، لا يظهر سجل العميل المقابل على الفور في المركز الرئيسي لـ Commerce.</span><span class="sxs-lookup"><span data-stu-id="861b4-106">When you create a new customer record by using the sign-up flow in the e-commerce storefront, the corresponding customer record doesn't immediately appear in Commerce headquarters.</span></span>

## <a name="resolution"></a><span data-ttu-id="861b4-107">الدقة</span><span class="sxs-lookup"><span data-stu-id="861b4-107">Resolution</span></span>

### <a name="disable-customer-creation-in-async-mode"></a><span data-ttu-id="861b4-108">تعطيل إنشاء العملاء في الوضع غير المتزامن</span><span class="sxs-lookup"><span data-stu-id="861b4-108">Disable customer creation in async mode</span></span>

> [!IMPORTANT]
> <span data-ttu-id="861b4-109">إذا قمت بتعطيل إنشاء عميل غير متزامن، فقد يتأثر أداء النظام، لأن إنشاء كل سجل سينتج طلبًا في الوقت الحقيقي إلى المركز الرئيسي لـ Commerce.</span><span class="sxs-lookup"><span data-stu-id="861b4-109">If you disable asynchronous customer creation, system performance could be affected, because creation of each record will produce a real-time request to Commerce headquarters.</span></span> <span data-ttu-id="861b4-110">بالإضافة إلى ذلك، إذا كان المركز الرئيسي لـ Commerce معطلًا (على سبيل المثال، أثناء تدفقات الصيانة)، فإن أي تدفقات إنشاء عميل جديد سوف تنتج أخطاء.</span><span class="sxs-lookup"><span data-stu-id="861b4-110">In addition, if Commerce headquarters is down (for example, during servicing flows), any new customer creation flows will produce errors.</span></span>

<span data-ttu-id="861b4-111">لتعطيل إنشاء العملاء في الوضع غير المتزامن في المركز الرئيسي لـ Commerce، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="861b4-111">To disable customer creation in async mode in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="861b4-112">انتقل إلى **Retail وCommerce \> إعداد القناة \> إعداد متجر على الإنترنت \> ملفات تعريف الوظائف**.</span><span class="sxs-lookup"><span data-stu-id="861b4-112">Go to **Retail and Commerce \> Channel setup \> Online store setup \> Functionality profiles**.</span></span>
1. <span data-ttu-id="861b4-113">إذا لم تكن تستخدم بالفعل ملف تعريف وظائف للقناة على الإنترنت، فقم بإنشاء واحد.</span><span class="sxs-lookup"><span data-stu-id="861b4-113">If you aren't already using a functionality profile for your online channel, create one.</span></span>
1. <span data-ttu-id="861b4-114">تأكد من تعيين الخيار **إنشاء عميل في الوضع غير متزامن** إلى **لا**.</span><span class="sxs-lookup"><span data-stu-id="861b4-114">Make sure that the **Create customer in async mode** option is set to **No**.</span></span>
1. <span data-ttu-id="861b4-115">انتقل إلى **Retail وCommerce \> القنوات \> المتاجر على الإنترنت**.</span><span class="sxs-lookup"><span data-stu-id="861b4-115">Go to **Retail and Commerce \> Channels \> Online stores**.</span></span>
1. <span data-ttu-id="861b4-116">حدد المتجر على الإنترنت لتعطيل إنشاء العميل غير المتزامن له.</span><span class="sxs-lookup"><span data-stu-id="861b4-116">Select the online store to disable asynchronous customer creation for.</span></span>
1. <span data-ttu-id="861b4-117">في علامة التبويب **عام**، تأكد من تعيين حقل **ملف تعريف الوظائف** على ملف تعريف الوظائف الذي تستخدمه في القناة على الإنترنت.</span><span class="sxs-lookup"><span data-stu-id="861b4-117">On the **General** tab, make sure that the **Functionality profile** field is set to the functionality profile that you're using for your online channel.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="861b4-118">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="861b4-118">Additional resources</span></span>

[<span data-ttu-id="861b4-119">إعداد مستأجر متاجرة عمل-مستهلك في Commerce</span><span class="sxs-lookup"><span data-stu-id="861b4-119">Setup a B2C tenant in Commerce</span></span>](../set-up-b2c-tenant.md)
