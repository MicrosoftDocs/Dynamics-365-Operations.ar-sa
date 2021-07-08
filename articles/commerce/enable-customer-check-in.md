---
title: تمكين إعلامات إيداع العملاء في نقطة البيع (POS)
description: يوضح هذا الموضوع كيفيه تمكين إعلامات إيداع العملاء في نقطة بيع Microsoft Dynamics 365 Commerce (POS).
author: bicyclingfool
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ROBOTS: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.author: stuharg
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: b42dc7766f8a69a7409c28d21b49cc96eca18dd4
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/17/2021
ms.locfileid: "6271415"
---
# <a name="enable-customer-check-in-notifications-in-point-of-sale-pos"></a><span data-ttu-id="a96c5-103">تمكين إعلامات إيداع العملاء في نقطة البيع (POS)</span><span class="sxs-lookup"><span data-stu-id="a96c5-103">Enable customer check-in notifications in point of sale (POS)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="a96c5-104">يوضح هذا الموضوع كيفيه تمكين إعلامات إيداع العملاء في نقطة بيع Microsoft Dynamics 365 Commerce (POS).</span><span class="sxs-lookup"><span data-stu-id="a96c5-104">This topic describes how to enable customer check-in notifications in Microsoft Dynamics 365 Commerce point of sale (POS).</span></span>

<span data-ttu-id="a96c5-105">في رسائل البريد الإلكتروني الخاصة بـ "الطلب جاهز للاستلام"، يمكن للمؤسسات توفير رابط أو زر يسمح للعملاء بإخطار المتجر بأنهم موجودون في المبنى وينتظرون إحضار الحزمة الخاصة بهم إليهم.</span><span class="sxs-lookup"><span data-stu-id="a96c5-105">In their "order ready for pickup" emails, organizations can provide a link or button that lets customers notify the store that they are on the premises and waiting for their package to be brought out to them.</span></span> <span data-ttu-id="a96c5-106">يتلقى العملاء بعد ذلك تأكيدًا لتسجيل الوصول، ويتلقى المتجر إشعارًا كمهمة في تطبيق نقطة البيع الخاص به.</span><span class="sxs-lookup"><span data-stu-id="a96c5-106">Customers then receive a check-in confirmation, and the store receives a notification as a task in its POS application.</span></span> <span data-ttu-id="a96c5-107">تعمل هذه المهمة كمطالبة بمساعد المبيعات لتسليم الأمر إلى سيارة العميل.</span><span class="sxs-lookup"><span data-stu-id="a96c5-107">This task serves as a prompt for a sales associate to deliver the order to the customer's vehicle.</span></span> <span data-ttu-id="a96c5-108">لذلك، لا يتعين على العميل الدخول إلى المتجر.</span><span class="sxs-lookup"><span data-stu-id="a96c5-108">Therefore, the customer doesn't have to enter the store.</span></span>

<span data-ttu-id="a96c5-109">يمكن أيضًا تكوين سير عمل تسجيل وصول العميل لجمع معلومات إضافية من العملاء، مثل رقم مكان وقوف السيارات الخاص بهم، والنوع، والطراز، ولون سيارتهم، وتعليمات التسليم.</span><span class="sxs-lookup"><span data-stu-id="a96c5-109">The customer check-in workflow can also be configured to collect additional information from customers, such as their parking spot number, the make, model, and color of their vehicle, and delivery instructions.</span></span> <span data-ttu-id="a96c5-110">يمكن لصاحب متجر البيع بالتجزئة استخدام هذه المعلومات لتسهيل تنفيذ الطلب.</span><span class="sxs-lookup"><span data-stu-id="a96c5-110">The retail store attendant can use this information to facilitate order fulfillment.</span></span>

## <a name="enable-customer-check-in"></a><span data-ttu-id="a96c5-111">تمكين إيداع العملاء</span><span class="sxs-lookup"><span data-stu-id="a96c5-111">Enable customer check-in</span></span>

<span data-ttu-id="a96c5-112">عند تشغيل ميزة إيداع العميل، تنشئ التجارة معرف تأكيد الطلب (المعروف أيضًا باسم معرف مرجع القناة).</span><span class="sxs-lookup"><span data-stu-id="a96c5-112">When the customer check-in feature is turned on, Commerce generates an order confirmation ID (also known as the channel reference ID).</span></span> <span data-ttu-id="a96c5-113">كما يقوم أيضًا بإنشاء معرفات تأكيد الطلب للأوامر التي تم إنشاؤها من خلال نقاط البيع (POS) أو قنوات مركز الاتصال.</span><span class="sxs-lookup"><span data-stu-id="a96c5-113">It also generates order confirmation IDs for orders that are created through point of sale (POS) or call center channels.</span></span> 

<span data-ttu-id="a96c5-114">لتشغيل ميزة إيداع العميل في المقر الرئيسي للتجارة، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="a96c5-114">To turn on the customer check-in feature in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="a96c5-115">انتقل إلى **مساحات العمل \> إدارة الميزات**.</span><span class="sxs-lookup"><span data-stu-id="a96c5-115">Go to **Workspaces \> Feature management**.</span></span>
2. <span data-ttu-id="a96c5-116">ابحث عن ميزة **إنشاء تنسيق معرف مرجعي ثابت للقناة عبر القنوات**.</span><span class="sxs-lookup"><span data-stu-id="a96c5-116">Search for the **Generate a consistent channel reference ID format across channels** feature.</span></span> 
3. <span data-ttu-id="a96c5-117">حدد الميزة، ثم حدد **تمكين الآن** في جزء الخصائص.</span><span class="sxs-lookup"><span data-stu-id="a96c5-117">Select the feature, and then select **Enable now** in the properties pane.</span></span> 

## <a name="create-a-check-in-confirmation-page"></a><span data-ttu-id="a96c5-118">إنشاء صفحة تأكيد الإيداع</span><span class="sxs-lookup"><span data-stu-id="a96c5-118">Create a check-in confirmation page</span></span>

<span data-ttu-id="a96c5-119">على موقع التجارة الإلكترونية الخاص بك، يجب عليك إنشاء صفحة جديدة ستكون بمثابة تجربة تأكيد الإيداع.</span><span class="sxs-lookup"><span data-stu-id="a96c5-119">On your e-commerce site, you must create a new page that will serve as the check-in confirmation experience.</span></span> <span data-ttu-id="a96c5-120">من خلال التكوين الإضافي، يمكن أن تتضمن الصفحة أيضًا نموذجًا يجمع معلومات إضافية من العملاء لتسهيل تنفيذ الطلبات.</span><span class="sxs-lookup"><span data-stu-id="a96c5-120">Through additional configuration, the page can also include a form that collects additional information from customers to facilitate order fulfillment.</span></span> <span data-ttu-id="a96c5-121">للحصول على معلومات حول كيفية إعداد الصفحة والوحدة، راجع [وحدة إيداع العميل](check-in-pickup-module.md).</span><span class="sxs-lookup"><span data-stu-id="a96c5-121">For information about how to set up the page and module, see [Customer check-in module](check-in-pickup-module.md).</span></span>

## <a name="configure-the-transactional-email-template"></a><span data-ttu-id="a96c5-122">تكوين قالب البريد الإلكتروني للحركات</span><span class="sxs-lookup"><span data-stu-id="a96c5-122">Configure the transactional email template</span></span>

<span data-ttu-id="a96c5-123">يجب عليك إضافة زر أو ارتباط **أنا هنا** إلى نموذج البريد الإلكتروني للحركات الذي يتلقاه العملاء عندما يكون طلبهم جاهزًا للاستلام.</span><span class="sxs-lookup"><span data-stu-id="a96c5-123">You must add an **I am here** link or button to the template for the transactional email that customers receive when their order is ready for pickup.</span></span> <span data-ttu-id="a96c5-124">سيستخدم العملاء هذا الرابط أو الزر لإخطار المتجر بوصولهم لاستلام طلباتهم.</span><span class="sxs-lookup"><span data-stu-id="a96c5-124">Customers will use this link or button to notify the store that they have arrived to pick up their order.</span></span> 

<span data-ttu-id="a96c5-125">أضف الارتباط أو الزر إلى القالب الذي تم تعيينه إلى نوع إعلام **اكتملت التعبئة** وطريقة التسليم التي تستخدمها لتنفيذ الطلبات على جانب الطريق.</span><span class="sxs-lookup"><span data-stu-id="a96c5-125">Add the link or button to the template that is mapped to the **Packing completed** notification type and the mode of delivery that you're using for curbside order fulfillment.</span></span> <span data-ttu-id="a96c5-126">في القالب، قم بإنشاء ارتباط HTML أو زر يشير إلى عنوان URL لصفحة تأكيد الإيداع التي قمت بإنشائها.</span><span class="sxs-lookup"><span data-stu-id="a96c5-126">In the template, create an HTML link or button that points to the URL of the check-in confirmation page that you created.</span></span> <span data-ttu-id="a96c5-127">فيما يلي مثال على ذلك.</span><span class="sxs-lookup"><span data-stu-id="a96c5-127">Here is an example.</span></span>

```
<a href="https://[YOUR_SITE_DOMAIN]/[CHECK-IN_CONFIRMATION_PAGE]?channelReferenceId=%channelreferenceid%&channelId=%channelid%&packingSlipId=%packingslipid%" target="_blank">I am here!</a>
```
<span data-ttu-id="a96c5-128">لمزيد من المعلومات حول كيفية تكوين قوالب البريد الإلكتروني، راجع [تخصيص رسائل البريد الإلكتروني للحركات حسب طريقة التسليم](customize-email-delivery-mode.md).</span><span class="sxs-lookup"><span data-stu-id="a96c5-128">For more information about how to configure email templates, see [Customize transactional emails by mode of delivery](customize-email-delivery-mode.md).</span></span> 

## <a name="a-check-in-confirmation-task-is-created-in-pos"></a><span data-ttu-id="a96c5-129">تم إنشاء مهمة تأكيد الإيداع في نقطة البيع</span><span class="sxs-lookup"><span data-stu-id="a96c5-129">A check-in confirmation task is created in POS</span></span>

<span data-ttu-id="a96c5-130">بعد أن يقوم العميل بإخطار المتجر بأنه موجود للاستلام، يتلقى إشعارًا بتأكيد تسجيل الوصول، ويتم إنشاء مهمة في قائمة المهام في نقطة البيع للمخزن حيث يقوم العميل باستلام الطلب.</span><span class="sxs-lookup"><span data-stu-id="a96c5-130">After a customer notifies the store that they are present for pickup, they receive a check-in confirmation notification, and a task is created in the tasks list in POS for the store where the customer is picking up the order.</span></span> <span data-ttu-id="a96c5-131">تحتوي المهمة على كافة معلومات العميل والأمر المطلوبة لاستيفاء الطلب.</span><span class="sxs-lookup"><span data-stu-id="a96c5-131">The task contains all the customer and order information that is required to fulfill the order.</span></span> <span data-ttu-id="a96c5-132">في المهمة، يُظهر حقل التعليمات أي معلومات تم جمعها من العميل من خلال نموذج المعلومات الإضافية.</span><span class="sxs-lookup"><span data-stu-id="a96c5-132">In the task, the instructions field shows any information that was collected from the customer through the additional information form.</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="a96c5-133">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="a96c5-133">Additional resources</span></span>

[<span data-ttu-id="a96c5-134">وحدة الإيداع للتسليم</span><span class="sxs-lookup"><span data-stu-id="a96c5-134">Check-in for pickup module</span></span>](check-in-pickup-module.md)
