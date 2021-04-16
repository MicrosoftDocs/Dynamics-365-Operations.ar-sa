---
title: إعداد بيئة تطوير التجارة الإلكترونية للتصحيح مقابل الجهاز الظاهري لملقم البيع بالتجزئة من المستوى الأول 1
description: يشرح هذا الموضوع كيفية إعداد بيئة تطوير التجارة الإلكترونية للتصحيح مقابل الجهاز الظاهري لملقم البيع بالتجزئة من المستوى الأول 1 (VM).
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
ms.openlocfilehash: 5ef286aa28ff459befb72b0178f308e5fb85ec44
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801473"
---
# <a name="set-up-an-e-commerce-development-environment-to-debug-against-a-tier-1-retail-server-virtual-machine"></a><span data-ttu-id="c9cad-103">إعداد بيئة تطوير التجارة الإلكترونية للتصحيح مقابل الجهاز الظاهري لملقم البيع بالتجزئة من المستوى الأول 1</span><span class="sxs-lookup"><span data-stu-id="c9cad-103">Set up an e-commerce development environment to debug against a Tier 1 Retail Server virtual machine</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c9cad-104">يشرح هذا الموضوع كيفية إعداد بيئة تطوير التجارة الإلكترونية للتصحيح مقابل الجهاز الظاهري لملقم البيع بالتجزئة من المستوى الأول 1 (VM).</span><span class="sxs-lookup"><span data-stu-id="c9cad-104">This topic explains how to set up an e-commerce development environment to debug against a Tier 1 Retail Server virtual machine (VM).</span></span>

## <a name="description"></a><span data-ttu-id="c9cad-105">الوصف</span><span class="sxs-lookup"><span data-stu-id="c9cad-105">Description</span></span>

<span data-ttu-id="c9cad-106">عادة ما يتم نشر بيئات Microsoft Dynamics 365 Commerce من المستوى 1 لتطوير ملحق Commerce runtime (CRT) ونقطة البيع (POS).</span><span class="sxs-lookup"><span data-stu-id="c9cad-106">Microsoft Dynamics 365 Commerce Tier 1 environments are typically deployed for Commerce runtime (CRT) and point of sale (POS) extension development.</span></span> <span data-ttu-id="c9cad-107">وهي بيئات مستقلة.</span><span class="sxs-lookup"><span data-stu-id="c9cad-107">They are standalone environments.</span></span> <span data-ttu-id="c9cad-108">وبسبب طبيعة بنية خدمة تأجير البرامج (SaaS)، فإنها لا تتضمن مكونات التجارة الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="c9cad-108">Because of the software as a service (SaaS) nature of the architecture, they don't include e-commerce components.</span></span>

<span data-ttu-id="c9cad-109">في بعض السيناريوهات، قد تحتاج إلى اختبار المكالمات إلى الملحقات في بيئة المستوى 1، بحيث يمكنك تصحيح الملحقات من مكونات التجارة الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="c9cad-109">In some scenarios, you might want to test calls to extensions in a Tier 1 environment, so that you can debug extensions from e-commerce components.</span></span> <span data-ttu-id="c9cad-110">للحصول على تعليمات عامة، راجع [تصحيح الأخطاء مقابل بيئة تطوير Commerce المستوى 1](../e-commerce-extensibility/debug-tier-1.md).</span><span class="sxs-lookup"><span data-stu-id="c9cad-110">For general instructions, see [Debug against a Tier 1 Commerce development environment](../e-commerce-extensibility/debug-tier-1.md).</span></span>

<span data-ttu-id="c9cad-111">عندما تقوم بالتصحيح مقابل بيئة المستوى 1، لأن الموقع يقوم الآن بالاتصال بخادم بيع بالتجزئة مختلف، فقد تتسبب المكالمات عبر الخوادم المتعددة في حدوث أخطاء مختلفة متعلقة بنهج أمان المحتوى.</span><span class="sxs-lookup"><span data-stu-id="c9cad-111">When you debug against a Tier 1 environment, because the site is now calling a different Retail Server, cross-server calls might cause various errors that are related to the content security policy.</span></span>

<span data-ttu-id="c9cad-112">يبين الرسم التوضيحي التالي مثالا للخطأ الذي قد يحدث عند تحديد متغير في صفحة تفاصيل المنتج.</span><span class="sxs-lookup"><span data-stu-id="c9cad-112">The following illustration shows an example of an error that might occur when a variant is selected on a product details page.</span></span>

![حدث خطأ عند تحديد متغير في إحدى صفحات تفاصيل المنتج](media/unhandled-rejection-error.jpg)

<span data-ttu-id="c9cad-114">يبين الرسم التوضيحي التالي مثالا لخطأ مشابه في أدوات مصحح أخطاء المستعرض (أدوات المطور F12).</span><span class="sxs-lookup"><span data-stu-id="c9cad-114">The following illustration shows an example of a similar error in a browser's debugger tools (F12 Developer Tools).</span></span> <span data-ttu-id="c9cad-115">تذكر رسالة الخطأ مخالفة توجيه نهج أمان المحتوى.</span><span class="sxs-lookup"><span data-stu-id="c9cad-115">The error message mentions violation of the content security policy directive.</span></span>

![خطأ في أدوات مصحح الأخطاء](media/debugger-tools-error.JPG)

## <a name="resolution"></a><span data-ttu-id="c9cad-117">الدقة</span><span class="sxs-lookup"><span data-stu-id="c9cad-117">Resolution</span></span>

### <a name="disable-the-content-security-policy-for-the-site-in-commerce-site-builder"></a><span data-ttu-id="c9cad-118">تعطيل نهج أمان المحتوى للموقع في منشئ مواقع Commerce</span><span class="sxs-lookup"><span data-stu-id="c9cad-118">Disable the content security policy for the site in Commerce site builder</span></span>

1. <span data-ttu-id="c9cad-119">حدد الموقع الذي تعمل عليه.</span><span class="sxs-lookup"><span data-stu-id="c9cad-119">Select the site that you're working on.</span></span>
1. <span data-ttu-id="c9cad-120">حدد **الإعدادات**، ثم حدد **الملحقات**.</span><span class="sxs-lookup"><span data-stu-id="c9cad-120">Select **Settings**, and then select **Extensions**.</span></span>
1. <span data-ttu-id="c9cad-121">في علامة التبويب **نهج أمان المحتوى**، حدد **تعطيل نهج أمان المحتوى**.</span><span class="sxs-lookup"><span data-stu-id="c9cad-121">On the **Content security policy** tab, select **Disable content security policy**.</span></span>
1. <span data-ttu-id="c9cad-122">حدد **حفظ ونشر**.</span><span class="sxs-lookup"><span data-stu-id="c9cad-122">Select **Save and publish**.</span></span>

> [!NOTE]
> <span data-ttu-id="c9cad-123">تسجيل الدخول إلى الشركة-المستهلك (B2C) لا يعمل في بيئة تطوير محلية.</span><span class="sxs-lookup"><span data-stu-id="c9cad-123">Business-to-consumer (B2C) sign-in won't work in a local development environment.</span></span> <span data-ttu-id="c9cad-124">مع ذلك، يمكنك استخدام عناصر وهمية صفحات السداد مع الخروج للضيف أو صفحات البناء لمحاكاة تسجيل دخول المستخدم كما هو مطلوب.</span><span class="sxs-lookup"><span data-stu-id="c9cad-124">However, you can use guest checkouts or build page mocks to simulate a user sign-in as required.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c9cad-125">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="c9cad-125">Additional resources</span></span>

[<span data-ttu-id="c9cad-126">‏‫بدء تطوير قابلية التوسع عبر الإنترنت للتجارة الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="c9cad-126">Get started with e-commerce online extensibility development</span></span>](../e-commerce-extensibility/sdk-getting-started.md)

[<span data-ttu-id="c9cad-127">إدارة نهج أمان المحتوى (CSP) في موقع التجارة الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="c9cad-127">Manage content security policy (CSP) on e-commerce site</span></span>](../manage-csp.md)
