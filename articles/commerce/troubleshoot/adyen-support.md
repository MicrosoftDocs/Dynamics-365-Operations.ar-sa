---
title: استكشاف أخطاء موصل دفع Dynamics 365 لمشكلات Adyen
description: يوفر هذا الموضوع إرشادات استكشاف الأخطاء وإصلاحها والتي يمكن أن تساعدك في الحصول على الدعم في حالة وجود مشكلات في موصل دفع Microsoft Dynamics 365 لـ Adyen.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
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
ms.openlocfilehash: 707efeba9553b996e4e33a4754e42a9d22643e33
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/11/2021
ms.locfileid: "6019579"
---
# <a name="troubleshoot-dynamics-365-payment-connector-for-adyen-issues"></a><span data-ttu-id="cffc7-103">استكشاف أخطاء موصل دفع Dynamics 365 لمشكلات Adyen</span><span class="sxs-lookup"><span data-stu-id="cffc7-103">Troubleshoot Dynamics 365 Payment Connector for Adyen issues</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="cffc7-104">يوفر هذا الموضوع إرشادات استكشاف الأخطاء وإصلاحها والتي يمكن أن تساعدك في الحصول على الدعم في حالة وجود مشكلات في موصل دفع Microsoft Dynamics 365 لـ Adyen.</span><span class="sxs-lookup"><span data-stu-id="cffc7-104">This topic provides troubleshooting guidance that can help you get support when you have issues with the Microsoft Dynamics 365 Payment Connector for Adyen.</span></span>

## <a name="description"></a><span data-ttu-id="cffc7-105">الوصف</span><span class="sxs-lookup"><span data-stu-id="cffc7-105">Description</span></span>

<span data-ttu-id="cffc7-106">لديك مشكلات في موصل دفع Dynamics 365 لـ Adyen في المناطق التالية، وطلبت الدعم من فريق Adyen:</span><span class="sxs-lookup"><span data-stu-id="cffc7-106">You have issues with the Dynamics 365 Payment Connector for Adyen in the following areas, and you require support from the Adyen team:</span></span>

- <span data-ttu-id="cffc7-107">تكوين نقطة البيع (POS) أو نقطة البيع الحديثة (MPOS) أو مركز الاتصال أو Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="cffc7-107">Configuration of Point of sale (POS), Modern point of sale (MPOS), call center, or Dynamics 365 Commerce</span></span>
- <span data-ttu-id="cffc7-108">رقم المرجع لموفر دفع لـ Adyen (PSP) (على سبيل المثال، إذا كان لديك أسئلة حول عمليات الرفض، يشمل ذلك عمليات رفض الإدخال اليدوي \[MKE\])</span><span class="sxs-lookup"><span data-stu-id="cffc7-108">The Adyen payment service provider (PSP) reference number (for example, if you have questions about refusals, including manual key entry \[MKE\] refusals)</span></span>
- <span data-ttu-id="cffc7-109">أي شيء لا يعمل في بيئات الاختبار أو التاجر المباشر</span><span class="sxs-lookup"><span data-stu-id="cffc7-109">Anything that isn't working in test or live merchant environments</span></span>

## <a name="resolution"></a><span data-ttu-id="cffc7-110">الدقة</span><span class="sxs-lookup"><span data-stu-id="cffc7-110">Resolution</span></span>

<span data-ttu-id="cffc7-111">استخدم قالب البريد الإلكتروني التالي لبدء عملية الدعم مع فريق Adyen.</span><span class="sxs-lookup"><span data-stu-id="cffc7-111">Use the following email template to start the support process with the Adyen team.</span></span> <span data-ttu-id="cffc7-112">للإسراع في استكشاف الأخطاء وإصلاحها، تأكد من احتواء البريد الإلكتروني على كافة التفاصيل المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="cffc7-112">To expedite troubleshooting, make sure that the email contains all the required details.</span></span>

| <span data-ttu-id="cffc7-113">الحقل</span><span class="sxs-lookup"><span data-stu-id="cffc7-113">Field</span></span>        | <span data-ttu-id="cffc7-114">قيمة</span><span class="sxs-lookup"><span data-stu-id="cffc7-114">Value</span></span> |
|--------------|-------|
| <span data-ttu-id="cffc7-115">إلى</span><span class="sxs-lookup"><span data-stu-id="cffc7-115">To</span></span>           | `support@adyen.com` |
| <span data-ttu-id="cffc7-116">نسخة</span><span class="sxs-lookup"><span data-stu-id="cffc7-116">Cc</span></span>           | |
| <span data-ttu-id="cffc7-117">سطر الموضوع</span><span class="sxs-lookup"><span data-stu-id="cffc7-117">Subject line</span></span> | <span data-ttu-id="cffc7-118">طلب دعم Microsoft Dynamics</span><span class="sxs-lookup"><span data-stu-id="cffc7-118">Microsoft Dynamics Support Request</span></span> |
| <span data-ttu-id="cffc7-119">النص الأساسي</span><span class="sxs-lookup"><span data-stu-id="cffc7-119">Body</span></span>         | <p><span data-ttu-id="cffc7-120">مرحبًا فريق الدعم،</span><span class="sxs-lookup"><span data-stu-id="cffc7-120">Hi Support,</span></span></p><p><span data-ttu-id="cffc7-121">الرجاء توفير الدعم للمشكلة التالية:</span><span class="sxs-lookup"><span data-stu-id="cffc7-121">Please provide support for the following issue:</span></span></p><ul><li><span data-ttu-id="cffc7-122">حساب التاجر</span><span class="sxs-lookup"><span data-stu-id="cffc7-122">Merchant account</span></span></li><li><span data-ttu-id="cffc7-123">البيئة (اختبار/إنتاج)</span><span class="sxs-lookup"><span data-stu-id="cffc7-123">Environment (Test/Prod)</span></span></li><li><span data-ttu-id="cffc7-124">القناة (نقطة بيع/مركز اتصال/تجارة إلكترونية عبر Commerce)</span><span class="sxs-lookup"><span data-stu-id="cffc7-124">Channel (POS/call center/Commerce e-commerce)</span></span></li><li><span data-ttu-id="cffc7-125">رقم مرجع PSP، إذا كانت المشكلة متضمنة لحركة محددة (يمكنك العثور على رقم مرجع PSP في الإيصال، في منطقة عملاء Adyen أو في قائمة الحركات في الوحدة الطرفية لنقطة البيع.)</span><span class="sxs-lookup"><span data-stu-id="cffc7-125">PSP reference number, if the issue involved a specific transaction (You can find the PSP reference number on the receipt, in the Adyen Customer Area, or on the transactions menu on the POS terminal.)</span></span></li><li><span data-ttu-id="cffc7-126">لقطة شاشة أو صورة لرسالة الخطأ، إذا كانت ممكنة</span><span class="sxs-lookup"><span data-stu-id="cffc7-126">Screenshot or photo of the error message, if applicable</span></span></li><li><span data-ttu-id="cffc7-127">سجلات عارض الأحداث (بتنسيق txt.)</span><span class="sxs-lookup"><span data-stu-id="cffc7-127">Event Viewer logs (in .txt format)</span></span></li><li><span data-ttu-id="cffc7-128">وصف المشكلة وخطوات استكشاف الأخطاء وإصلاحها التي حاولتها</span><span class="sxs-lookup"><span data-stu-id="cffc7-128">Description of the issue and troubleshooting steps that you've tried</span></span></li></ul> |

## <a name="additional-resources"></a><span data-ttu-id="cffc7-129">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="cffc7-129">Additional resources</span></span>

[<span data-ttu-id="cffc7-130">قبول المدفوعات باستخدام موصل Adyen لـ Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="cffc7-130">Accept payments with the Adyen connector for Dynamics 365 Commerce</span></span>](https://www.adyen.com/partners/dynamics-365-commerce)

[<span data-ttu-id="cffc7-131">موصل دفع Dynamics 365 لـ Adyen</span><span class="sxs-lookup"><span data-stu-id="cffc7-131">Dynamics 365 Payment Connector for Adyen</span></span>](../dev-itpro/adyen-connector.md)

[<span data-ttu-id="cffc7-132">إعداد موصل دفع Adyen لـ Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="cffc7-132">Set up the Adyen payment connector for Dynamics 365</span></span>](https://docs.adyen.com/plugins/microsoft-dynamics)
