---
title: استكشاف أخطاء موصل دفع Dynamics 365 لمشكلات Adyen
description: يوفر هذا الموضوع إرشادات استكشاف الأخطاء وإصلاحها والتي يمكن أن تساعدك في الحصول على الدعم في حالة وجود مشكلات في موصل دفع Microsoft Dynamics 365 لـ Adyen.
author: Reza-Assadi
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
ms.openlocfilehash: c779997d530d60f945bee19ee09bdabbff121fa6
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801809"
---
# <a name="troubleshoot-dynamics-365-payment-connector-for-adyen-issues"></a><span data-ttu-id="50f61-103">استكشاف أخطاء موصل دفع Dynamics 365 لمشكلات Adyen</span><span class="sxs-lookup"><span data-stu-id="50f61-103">Troubleshoot Dynamics 365 Payment Connector for Adyen issues</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="50f61-104">يوفر هذا الموضوع إرشادات استكشاف الأخطاء وإصلاحها والتي يمكن أن تساعدك في الحصول على الدعم في حالة وجود مشكلات في موصل دفع Microsoft Dynamics 365 لـ Adyen.</span><span class="sxs-lookup"><span data-stu-id="50f61-104">This topic provides troubleshooting guidance that can help you get support when you have issues with the Microsoft Dynamics 365 Payment Connector for Adyen.</span></span>

## <a name="description"></a><span data-ttu-id="50f61-105">الوصف</span><span class="sxs-lookup"><span data-stu-id="50f61-105">Description</span></span>

<span data-ttu-id="50f61-106">لديك مشكلات في موصل دفع Dynamics 365 لـ Adyen في المناطق التالية، وطلبت الدعم من فريق Adyen:</span><span class="sxs-lookup"><span data-stu-id="50f61-106">You have issues with the Dynamics 365 Payment Connector for Adyen in the following areas, and you require support from the Adyen team:</span></span>

- <span data-ttu-id="50f61-107">تكوين نقطة البيع (POS) أو نقطة البيع الحديثة (MPOS) أو مركز الاتصال أو Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="50f61-107">Configuration of Point of sale (POS), Modern point of sale (MPOS), call center, or Dynamics 365 Commerce</span></span>
- <span data-ttu-id="50f61-108">رقم المرجع لموفر دفع لـ Adyen (PSP) (على سبيل المثال، إذا كان لديك أسئلة حول عمليات الرفض، يشمل ذلك عمليات رفض الإدخال اليدوي \[MKE\])</span><span class="sxs-lookup"><span data-stu-id="50f61-108">The Adyen payment service provider (PSP) reference number (for example, if you have questions about refusals, including manual key entry \[MKE\] refusals)</span></span>
- <span data-ttu-id="50f61-109">أي شيء لا يعمل في بيئات الاختبار أو التاجر المباشر</span><span class="sxs-lookup"><span data-stu-id="50f61-109">Anything that isn't working in test or live merchant environments</span></span>

## <a name="resolution"></a><span data-ttu-id="50f61-110">الدقة</span><span class="sxs-lookup"><span data-stu-id="50f61-110">Resolution</span></span>

<span data-ttu-id="50f61-111">استخدم قالب البريد الإلكتروني التالي لبدء عملية الدعم مع فريق Adyen.</span><span class="sxs-lookup"><span data-stu-id="50f61-111">Use the following email template to start the support process with the Adyen team.</span></span> <span data-ttu-id="50f61-112">للإسراع في استكشاف الأخطاء وإصلاحها، تأكد من احتواء البريد الإلكتروني على كافة التفاصيل المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="50f61-112">To expedite troubleshooting, make sure that the email contains all the required details.</span></span>

| <span data-ttu-id="50f61-113">الحقل</span><span class="sxs-lookup"><span data-stu-id="50f61-113">Field</span></span>        | <span data-ttu-id="50f61-114">قيمة</span><span class="sxs-lookup"><span data-stu-id="50f61-114">Value</span></span> |
|--------------|-------|
| <span data-ttu-id="50f61-115">إلى</span><span class="sxs-lookup"><span data-stu-id="50f61-115">To</span></span>           | `support@adyen.com` |
| <span data-ttu-id="50f61-116">نسخة</span><span class="sxs-lookup"><span data-stu-id="50f61-116">Cc</span></span>           | |
| <span data-ttu-id="50f61-117">سطر الموضوع</span><span class="sxs-lookup"><span data-stu-id="50f61-117">Subject line</span></span> | <span data-ttu-id="50f61-118">طلب دعم Microsoft Dynamics</span><span class="sxs-lookup"><span data-stu-id="50f61-118">Microsoft Dynamics Support Request</span></span> |
| <span data-ttu-id="50f61-119">النص الأساسي</span><span class="sxs-lookup"><span data-stu-id="50f61-119">Body</span></span>         | <p><span data-ttu-id="50f61-120">مرحبًا فريق الدعم،</span><span class="sxs-lookup"><span data-stu-id="50f61-120">Hi Support,</span></span></p><p><span data-ttu-id="50f61-121">الرجاء توفير الدعم للمشكلة التالية:</span><span class="sxs-lookup"><span data-stu-id="50f61-121">Please provide support for the following issue:</span></span></p><ul><li><span data-ttu-id="50f61-122">حساب التاجر</span><span class="sxs-lookup"><span data-stu-id="50f61-122">Merchant account</span></span></li><li><span data-ttu-id="50f61-123">البيئة (اختبار/إنتاج)</span><span class="sxs-lookup"><span data-stu-id="50f61-123">Environment (Test/Prod)</span></span></li><li><span data-ttu-id="50f61-124">القناة (نقطة بيع/مركز اتصال/تجارة إلكترونية عبر Commerce)</span><span class="sxs-lookup"><span data-stu-id="50f61-124">Channel (POS/call center/Commerce e-commerce)</span></span></li><li><span data-ttu-id="50f61-125">رقم مرجع PSP، إذا كانت المشكلة متضمنة لحركة محددة (يمكنك العثور على رقم مرجع PSP في الإيصال، في منطقة عملاء Adyen أو في قائمة الحركات في الوحدة الطرفية لنقطة البيع.)</span><span class="sxs-lookup"><span data-stu-id="50f61-125">PSP reference number, if the issue involved a specific transaction (You can find the PSP reference number on the receipt, in the Adyen Customer Area, or on the transactions menu on the POS terminal.)</span></span></li><li><span data-ttu-id="50f61-126">لقطة شاشة أو صورة لرسالة الخطأ، إذا كانت ممكنة</span><span class="sxs-lookup"><span data-stu-id="50f61-126">Screenshot or photo of the error message, if applicable</span></span></li><li><span data-ttu-id="50f61-127">سجلات عارض الأحداث (بتنسيق txt.)</span><span class="sxs-lookup"><span data-stu-id="50f61-127">Event Viewer logs (in .txt format)</span></span></li><li><span data-ttu-id="50f61-128">وصف المشكلة وخطوات استكشاف الأخطاء وإصلاحها التي حاولتها</span><span class="sxs-lookup"><span data-stu-id="50f61-128">Description of the issue and troubleshooting steps that you've tried</span></span></li></ul> |

## <a name="additional-resources"></a><span data-ttu-id="50f61-129">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="50f61-129">Additional resources</span></span>

[<span data-ttu-id="50f61-130">قبول المدفوعات باستخدام موصل Adyen لـ Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="50f61-130">Accept payments with the Adyen connector for Dynamics 365 Commerce</span></span>](https://www.adyen.com/partners/dynamics-365-commerce)

[<span data-ttu-id="50f61-131">موصل دفع Dynamics 365 لـ Adyen</span><span class="sxs-lookup"><span data-stu-id="50f61-131">Dynamics 365 Payment Connector for Adyen</span></span>](../dev-itpro/adyen-connector.md)

[<span data-ttu-id="50f61-132">إعداد موصل دفع Adyen لـ Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="50f61-132">Set up the Adyen payment connector for Dynamics 365</span></span>](https://docs.adyen.com/plugins/microsoft-dynamics)
