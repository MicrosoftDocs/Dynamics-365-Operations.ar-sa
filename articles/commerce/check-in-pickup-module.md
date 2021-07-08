---
title: وحدة الإيداع للالتقاط
description: يغطي هذا الموضوع وحدة الإيداع للالتقاط ويشرح كيفية تكوينها في Microsoft Dynamics 365 Commerce.
author: bicyclingfool
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ROBOTS: ''
audience: Application user
ms.reviewer: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.author: stuharg
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 0baa922afc72778dd6e4836398a280cbe6abaec2
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/17/2021
ms.locfileid: "6270573"
---
# <a name="check-in-for-pickup-module"></a><span data-ttu-id="7e3cd-103">وحدة الإيداع للالتقاط</span><span class="sxs-lookup"><span data-stu-id="7e3cd-103">Check-in for pickup module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="7e3cd-104">يغطي هذا الموضوع وحدة الإيداع للالتقاط ويشرح كيفية تكوينها في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="7e3cd-104">This topic covers the check-in for pickup module and explains how to configure it in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="7e3cd-105">توفر وحدة الإيداع للالتقاط صفحة تأكيد للعملاء الذين يستخدمون إمكانات التحقق من عملاء Dynamics 365 Commerce لإخطار المتجر بوصولهم.</span><span class="sxs-lookup"><span data-stu-id="7e3cd-105">The check-in for pickup module provides a confirmation page for customers who use the Dynamics 365 Commerce customer check-in capabilities to notify a store about their arrival.</span></span> <span data-ttu-id="7e3cd-106">تتيح لك وحدة الإيداع للالتقاط أيضًا تكوين نموذج يجمع معلومات إضافية من العملاء لتسهيل تسليم الأوامر.</span><span class="sxs-lookup"><span data-stu-id="7e3cd-106">The check-in for pickup module also lets you configure a form that collects additional information from customers to facilitate order delivery.</span></span> <span data-ttu-id="7e3cd-107">تتضمن هذه المعلومات رقم مكان وقوف العميل، ونوع وطراز سيارته.</span><span class="sxs-lookup"><span data-stu-id="7e3cd-107">This information includes a customer's parking spot number, and the make and model of their vehicle.</span></span> 

## <a name="module-properties"></a><span data-ttu-id="7e3cd-108">خصائص الوحدة النمطية</span><span class="sxs-lookup"><span data-stu-id="7e3cd-108">Module properties</span></span>

| <span data-ttu-id="7e3cd-109">اسم الخاصية</span><span class="sxs-lookup"><span data-stu-id="7e3cd-109">Property name</span></span> | <span data-ttu-id="7e3cd-110">القيم</span><span class="sxs-lookup"><span data-stu-id="7e3cd-110">Values</span></span> | <span data-ttu-id="7e3cd-111">الوصف</span><span class="sxs-lookup"><span data-stu-id="7e3cd-111">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="7e3cd-112">نص التأكيد</span><span class="sxs-lookup"><span data-stu-id="7e3cd-112">Confirmation text</span></span> | <span data-ttu-id="7e3cd-113">سلسلة نص</span><span class="sxs-lookup"><span data-stu-id="7e3cd-113">Text string</span></span> | <span data-ttu-id="7e3cd-114">محتوى العنوان الذي يظهر في صفحة تأكيد الإيداع.</span><span class="sxs-lookup"><span data-stu-id="7e3cd-114">Content for the heading that appears on the check-in confirmation page.</span></span> |
| <span data-ttu-id="7e3cd-115">عرض ‏‫كود الاستجابة السريعة (QR)‬</span><span class="sxs-lookup"><span data-stu-id="7e3cd-115">Show QR code</span></span> | <span data-ttu-id="7e3cd-116">**صحيح** أم **خطأ**</span><span class="sxs-lookup"><span data-stu-id="7e3cd-116">**True** or **False**</span></span> | <span data-ttu-id="7e3cd-117">عند تعيين هذه الخاصية إلى **True**، تقوم صفحه تأكيد الإيداع بإظهار كود الاستجابة السريعة (QR) الذي يمثل معرف تأكيد الأمر.</span><span class="sxs-lookup"><span data-stu-id="7e3cd-117">When this property is set to **True**, the check-in confirmation page shows a QR code that represents the order confirmation ID.</span></span> |
| <span data-ttu-id="7e3cd-118">عنوان المعلومات الإضافية</span><span class="sxs-lookup"><span data-stu-id="7e3cd-118">Additional information heading</span></span> | <span data-ttu-id="7e3cd-119">سلسلة نص</span><span class="sxs-lookup"><span data-stu-id="7e3cd-119">Text string</span></span> | <span data-ttu-id="7e3cd-120">محتوى العنوان الذي يظهر عند تكوين حقول معلومات إضافية.</span><span class="sxs-lookup"><span data-stu-id="7e3cd-120">Content for the heading that appears when additional information fields have been configured.</span></span> |
| <span data-ttu-id="7e3cd-121">مفاتيح المعلومات الإضافية</span><span class="sxs-lookup"><span data-stu-id="7e3cd-121">Additional information keys</span></span> | <span data-ttu-id="7e3cd-122">زوج قيمة المورد/معرف المورد</span><span class="sxs-lookup"><span data-stu-id="7e3cd-122">Resource ID/resource value pair</span></span> | <span data-ttu-id="7e3cd-123">يقوم كل مفتاح بإنشاء حقل نموذج وتسمية مقترنة يتم استخدامها لجمع معلومات إضافية من العملاء.</span><span class="sxs-lookup"><span data-stu-id="7e3cd-123">Each key creates a form field and an associated label that are used to collect additional information from customers.</span></span> |
| <span data-ttu-id="7e3cd-124">مفاتيح المعلومات الإضافية \> معرف المورد</span><span class="sxs-lookup"><span data-stu-id="7e3cd-124">Additional information keys \> Resource ID</span></span> | <span data-ttu-id="7e3cd-125">سلسلة نص</span><span class="sxs-lookup"><span data-stu-id="7e3cd-125">Text string</span></span> | <span data-ttu-id="7e3cd-126">يقوم كل مفتاح معلومات بإنشاء حقل نموذج وتسمية مقترنة يتم استخدامها لجمع معلومات إضافية من العملاء.</span><span class="sxs-lookup"><span data-stu-id="7e3cd-126">Each information key creates a form field and an associated label that are used to collect additional information from customers.</span></span> <span data-ttu-id="7e3cd-127">تحدد هذه الخاصية مفتاح المعلومات الإضافية.</span><span class="sxs-lookup"><span data-stu-id="7e3cd-127">This property identifies the additional information key.</span></span> <span data-ttu-id="7e3cd-128">في المهمة التي تم إنشاؤها في نقطة البيع (POS)، يتم عرض قيمة هذه الخاصية كتسمية في حقل التعليمات.</span><span class="sxs-lookup"><span data-stu-id="7e3cd-128">In the task that is created in point of sale (POS), the value of this property is shown as the label in the instructions field.</span></span> |
| <span data-ttu-id="7e3cd-129">مفاتيح المعلومات الإضافية \> قيمة المورد</span><span class="sxs-lookup"><span data-stu-id="7e3cd-129">Additional information keys \> Resource value</span></span> | <span data-ttu-id="7e3cd-130">سلسلة نص</span><span class="sxs-lookup"><span data-stu-id="7e3cd-130">Text string</span></span> | <span data-ttu-id="7e3cd-131">التسمية الخاصة بحقل النص في المهمة الموجودة في نقطه البيع.</span><span class="sxs-lookup"><span data-stu-id="7e3cd-131">The label for the text field in the task in POS.</span></span> |
| <span data-ttu-id="7e3cd-132">مفاتيح المعلومات الإضافية \> مطلوبة</span><span class="sxs-lookup"><span data-stu-id="7e3cd-132">Additional information keys \> Required</span></span> | <span data-ttu-id="7e3cd-133">**صحيح** أم **خطأ**</span><span class="sxs-lookup"><span data-stu-id="7e3cd-133">**True** or **False**</span></span> | <span data-ttu-id="7e3cd-134">تحدد هذه الخاصية ما إذا كان يجب على العملاء ملء حقل النموذج قبل أن يتمكنوا من المتابعة.</span><span class="sxs-lookup"><span data-stu-id="7e3cd-134">This property specifies whether customers must fill in the form field before they can continue.</span></span> <span data-ttu-id="7e3cd-135">عند تعيين هذه الخاصية إلى **True**، يتم عرض علامة النجمة بجوار ملصق النموذج، ويتم إجراء فحص فارغ لمنع العملاء من الاستمرار في حالة عدم إدخال أي قيمة.</span><span class="sxs-lookup"><span data-stu-id="7e3cd-135">When this property is set to **True**, an asterisk is rendered next to the form label, and a null check is done to prevent customers from continuing if no value is entered.</span></span> |

## <a name="add-the-check-in-for-pickup-module-to-a-page"></a><span data-ttu-id="7e3cd-136">إضافة وحدة الإيداع للالتقاط إلى صفحة</span><span class="sxs-lookup"><span data-stu-id="7e3cd-136">Add the check-in for pickup module to a page</span></span>

<span data-ttu-id="7e3cd-137">يجب إضافة وحدة الإيداع للالتقاط إلى الصفحة الجديدة التي تقوم بإنشائها لتأكيد الإيداع.</span><span class="sxs-lookup"><span data-stu-id="7e3cd-137">The check-in for pickup module should be added to the new page that you create for check-in confirmation.</span></span> <span data-ttu-id="7e3cd-138">ستعمل هذه الصفحة كتجربة تأكيد الإيداع للعملاء الذين يحددون ارتباط أو زر **أنا هنا** في رسالة بريدهم الإلكتروني.</span><span class="sxs-lookup"><span data-stu-id="7e3cd-138">That page will serve as the check-in confirmation experience for customers who select the **I am here** link or button in their email.</span></span> 

## <a name="configure-the-additional-information-form"></a><span data-ttu-id="7e3cd-139">تكوين نموذج المعلومات الإضافية</span><span class="sxs-lookup"><span data-stu-id="7e3cd-139">Configure the additional information form</span></span>

<span data-ttu-id="7e3cd-140">بشكل افتراضي، إذا لم يتم تكوين مفاتيح معلومات إضافية، تعرض الوحدة للعملاء صفحة تأكيد الإيداع.</span><span class="sxs-lookup"><span data-stu-id="7e3cd-140">By default, if no additional information keys are configured, the module shows customers the check-in confirmation page.</span></span> <span data-ttu-id="7e3cd-141">أثناء عرض تأكيد الإيداع، يتم إنشاء مهمة في نقطة البيع للمخزن حيث يتم التقاط الأمر.</span><span class="sxs-lookup"><span data-stu-id="7e3cd-141">As the check-in confirmation is shown, a task is created in POS for the store where the order is being picked up.</span></span>

<span data-ttu-id="7e3cd-142">عند تكوين مفتاح معلومات إضافي واحد أو أكثر، يُطلب من العملاء أولاً إدخال المعلومات.</span><span class="sxs-lookup"><span data-stu-id="7e3cd-142">When one or more additional information keys are configured, customers are first prompted to enter information.</span></span> <span data-ttu-id="7e3cd-143">عند تحديد **إرسال**، يتم عرض تأكيد الإيداع، ويتم إنشاء مهمة في نقطة البيع.</span><span class="sxs-lookup"><span data-stu-id="7e3cd-143">When they select **Submit**, they are shown the check-in confirmation, and a task is created in POS.</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="7e3cd-144">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="7e3cd-144">Additional resources</span></span>

[<span data-ttu-id="7e3cd-145">تمكين إعلامات إيداع العملاء في نقطة البيع (POS)</span><span class="sxs-lookup"><span data-stu-id="7e3cd-145">Enable customer check-in notifications in point of sale (POS)</span></span>](enable-customer-check-in.md)
