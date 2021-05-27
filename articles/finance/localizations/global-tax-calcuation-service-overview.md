---
title: (إصدار أولي) حساب الضرائب
description: يوضح هذا الموضوع النطاق الإجمالي والميزات الخاصة بقدرة حساب الضريبة.
author: wangchen
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: b26472e195d9bdbba340a118c106de1a4dc79b34
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021922"
---
# <a name="tax-calculation-preview"></a><span data-ttu-id="80f80-103">(إصدار أولي) حساب الضرائب</span><span class="sxs-lookup"><span data-stu-id="80f80-103">Tax Calculation (Preview)</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="80f80-104">خدمة حساب الضريبة هي خدمة متعددة المستأجرين قابلة للتوسع بشكل كبير وتمكّن Global Tax Engine من أتمتة وتبسيط عملية تحديد الضرائب وحسابها.</span><span class="sxs-lookup"><span data-stu-id="80f80-104">Tax Calculation is a hyper-scalable multitenant service that enables the global tax engine to automate and simplify the tax determination and calculation process.</span></span> <span data-ttu-id="80f80-105">محرك الضرائب قابل للتكوين بالكامل.</span><span class="sxs-lookup"><span data-stu-id="80f80-105">The tax engine is fully configurable.</span></span> <span data-ttu-id="80f80-106">تتضمن العناصر التي يمكن تكوينها، على سبيل المثال لا الحصر، نموذج البيانات الخاضع للضريبة، وكود الضريبة، ومصفوفة تطبيق الضريبة، وصيغة حساب الضريبة.</span><span class="sxs-lookup"><span data-stu-id="80f80-106">The elements that can be configured include, but aren't limited to, the taxable data model, tax code, tax applicability matrix, and tax calculation formula.</span></span> <span data-ttu-id="80f80-107">يعمل محرك الضرائب على النظام الأساسي لخدمات Microsoft Azure الأساسية، ويقدم التكنولوجيا الحديثة وقابلية التوسع الأسي.</span><span class="sxs-lookup"><span data-stu-id="80f80-107">The tax engine runs on the Microsoft Azure core services platform, and offers modern technology and exponential scalability.</span></span>

<span data-ttu-id="80f80-108">تتكامل خدمه حساب الضريبة مع Dynamics 365 Finance وDynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="80f80-108">Tax Calculation integrates with Dynamics 365 Finance and Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="80f80-109">وأخيرُا، ستقوم أيضا بالتكامل مع Dynamics 365 Project Operations وDynamics 365 Commerce وتطبيقات أخرى تابعة للجهات الخارجية والجهات الأولى.</span><span class="sxs-lookup"><span data-stu-id="80f80-109">Eventually, it will also integrate with Dynamics 365 Project Operations, Dynamics 365 Commerce, and other first-party and third-party applications.</span></span>

<span data-ttu-id="80f80-110">خدمة حساب الضريبة هي محرك ضرائب قائم على الخدمات الصغيرة يوفر قابلية توسعة أسية.</span><span class="sxs-lookup"><span data-stu-id="80f80-110">Tax Calculation is a microservice-based tax engine that offers exponential scalability.</span></span> <span data-ttu-id="80f80-111">يمكن أن تساعدك في أداء المهام التالية:</span><span class="sxs-lookup"><span data-stu-id="80f80-111">It can help you perform the following tasks:</span></span>

- <span data-ttu-id="80f80-112">تكوين حساب الضريبة من خلال Regulatory Configuration Service (RCS).</span><span class="sxs-lookup"><span data-stu-id="80f80-112">Configure Tax Calculation through Regulatory Configuration Service (RCS).</span></span> <span data-ttu-id="80f80-113">إن RCS هي نسخة محسنة من مصمم التقارير الإلكترونية (ER) وهي متاح كخدمة قائمة بذاتها.</span><span class="sxs-lookup"><span data-stu-id="80f80-113">RCS is an enhanced version of the Electronic reporting (ER) designer and is available as a standalone service.</span></span>
- <span data-ttu-id="80f80-114">تكوين مصفوفة الضرائب لتحديد أكواد الضرائب ومعدلاتها تلقائيًا.</span><span class="sxs-lookup"><span data-stu-id="80f80-114">Configure the tax matrix to automatically determine tax codes and rates.</span></span>
- <span data-ttu-id="80f80-115">تكوين مصفوفة الضرائب لتحديد رقم التسجيل الضريبي تلقائيًا.</span><span class="sxs-lookup"><span data-stu-id="80f80-115">Configure the tax matrix to automatically determine the tax registration number.</span></span>
- <span data-ttu-id="80f80-116">تكوين مصمم حساب الضريبة لتحديد الصيغ والشروط.</span><span class="sxs-lookup"><span data-stu-id="80f80-116">Configure the tax calculation designer to define formulas and conditions.</span></span>
- <span data-ttu-id="80f80-117">مشاركة حل تحديد الضريبة وحسابها عبر الكيانات القانونية.</span><span class="sxs-lookup"><span data-stu-id="80f80-117">Share the tax determination and calculation solution across legal entities.</span></span>

<span data-ttu-id="80f80-118">لاستخدام خدمة حساب الضريبة، قم بتثبيت الوظيفة الإضافية لخدمة حساب الضريبة من مشروعك في Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="80f80-118">To use the tax calculation service, install the tax calculation service add-in from your project in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="80f80-119">ثم أكمل الإعداد في RCS، وقم بتمكين خدمة حساب الضريبة في Finance وSupply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="80f80-119">Then complete the setup in RCS, and enable the tax calculation service in Finance and Supply Chain Management.</span></span> <span data-ttu-id="80f80-120">لمزيد من المعلومات، راجع [بدء استخدام خدمة الضريبة](./global-get-started-with-tax-calculation-service.md).</span><span class="sxs-lookup"><span data-stu-id="80f80-120">For more information, see [Get started with tax service](./global-get-started-with-tax-calculation-service.md).</span></span>

## <a name="availability"></a><span data-ttu-id="80f80-121">التوفر</span><span class="sxs-lookup"><span data-stu-id="80f80-121">Availability</span></span>

<span data-ttu-id="80f80-122">خدمة حساب الضريبة متاحة فقط في بيئات آلية تحديد الصلاحيات ولعملاء محددين، من خلال برنامج الإصدار الأولي.</span><span class="sxs-lookup"><span data-stu-id="80f80-122">Tax Calculation is available only in sandbox environments and to selected customers, through a public preview program.</span></span> <span data-ttu-id="80f80-123">في النهاية، ستصبح متاحة بشكل عام لجميع العملاء وفي بيئات الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="80f80-123">Eventually, it will become generally available to all customers and in production environments.</span></span>

<span data-ttu-id="80f80-124">سيستمر تسليم الميزات الجديدة، لذا تأكد من مراجعة أحدث الوثائق في كثير من الأحيان للتعرف على تغطية ونطاق الميزات المدعومة.</span><span class="sxs-lookup"><span data-stu-id="80f80-124">New features will continue to be delivered, so be sure to check the most up-to-date documentation often to learn about the coverage and scope of supported features.</span></span>

<span data-ttu-id="80f80-125">يتم نشر خدمة حساب الضريبة في مناطق Azure الجغرافية التالية.</span><span class="sxs-lookup"><span data-stu-id="80f80-125">Tax Calculation is deployed in the following Azure geographies.</span></span> <span data-ttu-id="80f80-126">سيتم نشره أيضًا في المزيد من مناطق Azure الجغرافية، بناءً على احتياجات العملاء:</span><span class="sxs-lookup"><span data-stu-id="80f80-126">It will also be deployed to more Azure geographies, based on customer needs:</span></span>

- <span data-ttu-id="80f80-127">الولايات المتحدة</span><span class="sxs-lookup"><span data-stu-id="80f80-127">United States</span></span>
- <span data-ttu-id="80f80-128">أوروبا</span><span class="sxs-lookup"><span data-stu-id="80f80-128">Europe</span></span>

> [!NOTE]
> <span data-ttu-id="80f80-129">لا تدعم خدمة حساب الضريبة عمليات النشر المحلية لـ Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="80f80-129">Tax Calculation doesn't support on-premises deployments of Dynamics 365.</span></span> <span data-ttu-id="80f80-130">كما أنه لا يدعم الإصدارات السابقة، مثل Dynamics AX 2012.</span><span class="sxs-lookup"><span data-stu-id="80f80-130">It also doesn't support earlier versions, such as Dynamics AX 2012.</span></span>

## <a name="feature-highlights"></a><span data-ttu-id="80f80-131">النقاط الرئيسية في الميزات</span><span class="sxs-lookup"><span data-stu-id="80f80-131">Feature highlights</span></span>

- <span data-ttu-id="80f80-132">مصفوفة ضرائب قابلة للتكوين لتحديد الضريبة وحسابها تلقائيًا</span><span class="sxs-lookup"><span data-stu-id="80f80-132">A configurable tax matrix to automatically determine and calculate tax</span></span>
- <span data-ttu-id="80f80-133">دعم لأرقام تسجيل الضريبة المتعددة</span><span class="sxs-lookup"><span data-stu-id="80f80-133">Support for multiple tax registration numbers</span></span>
- <span data-ttu-id="80f80-134">دعم أمر التحويل لتحديد الضرائب وحسابها</span><span class="sxs-lookup"><span data-stu-id="80f80-134">Transfer order support for tax determination and calculation</span></span>
- <span data-ttu-id="80f80-135">دعم أمر التحويل لتحديد أرقام تسجيل متعددة للضريبة</span><span class="sxs-lookup"><span data-stu-id="80f80-135">Transfer order support for determination of multiple tax registration numbers</span></span>

## <a name="supported-transactions"></a><span data-ttu-id="80f80-136">الحركات المدعومة</span><span class="sxs-lookup"><span data-stu-id="80f80-136">Supported transactions</span></span>

<span data-ttu-id="80f80-137">يمكن تمكين خدمة حساب الضريبة بواسطة الكيان القانوني والحركة.</span><span class="sxs-lookup"><span data-stu-id="80f80-137">Tax Calculation can be enabled by legal entity and transaction.</span></span> <span data-ttu-id="80f80-138">الحركات التالية مدعومة:</span><span class="sxs-lookup"><span data-stu-id="80f80-138">The following transactions are supported:</span></span>

- <span data-ttu-id="80f80-139">عملية المبيعات</span><span class="sxs-lookup"><span data-stu-id="80f80-139">Sales process</span></span>

    - <span data-ttu-id="80f80-140">عرض أسعار المبيعات</span><span class="sxs-lookup"><span data-stu-id="80f80-140">Sales quotation</span></span>
    - <span data-ttu-id="80f80-141">أمر مبيعات</span><span class="sxs-lookup"><span data-stu-id="80f80-141">Sales order</span></span>
    - <span data-ttu-id="80f80-142">التأكيد</span><span class="sxs-lookup"><span data-stu-id="80f80-142">Confirmation</span></span>
    - <span data-ttu-id="80f80-143">قائمة الانتقاء</span><span class="sxs-lookup"><span data-stu-id="80f80-143">Picking list</span></span>
    - <span data-ttu-id="80f80-144">إيصال التعبئة</span><span class="sxs-lookup"><span data-stu-id="80f80-144">Packing slip</span></span>
    - <span data-ttu-id="80f80-145">فاتورة المبيعات</span><span class="sxs-lookup"><span data-stu-id="80f80-145">Sales invoice</span></span>
    - <span data-ttu-id="80f80-146">إشعار دائن</span><span class="sxs-lookup"><span data-stu-id="80f80-146">Credit note</span></span>
    - <span data-ttu-id="80f80-147">أمر الإرجاع</span><span class="sxs-lookup"><span data-stu-id="80f80-147">Return order</span></span>
    - <span data-ttu-id="80f80-148">تكلفة رسوم متنوعة</span><span class="sxs-lookup"><span data-stu-id="80f80-148">Header miscellaneous charge</span></span>
    - <span data-ttu-id="80f80-149">تكلفة الخط المتنوعة</span><span class="sxs-lookup"><span data-stu-id="80f80-149">Line miscellaneous charge</span></span>

- <span data-ttu-id="80f80-150">عمليه الشراء</span><span class="sxs-lookup"><span data-stu-id="80f80-150">Purchase process</span></span>

    - <span data-ttu-id="80f80-151">أمر شراء</span><span class="sxs-lookup"><span data-stu-id="80f80-151">Purchase order</span></span>
    - <span data-ttu-id="80f80-152">التأكيد</span><span class="sxs-lookup"><span data-stu-id="80f80-152">Confirmation</span></span>
    - <span data-ttu-id="80f80-153">قائمة الإيصالات</span><span class="sxs-lookup"><span data-stu-id="80f80-153">Receipts list</span></span>
    - <span data-ttu-id="80f80-154">إيصال استلام المنتج</span><span class="sxs-lookup"><span data-stu-id="80f80-154">Product receipt</span></span>
    - <span data-ttu-id="80f80-155">فاتورة الشراء</span><span class="sxs-lookup"><span data-stu-id="80f80-155">Purchase invoice</span></span>
    - <span data-ttu-id="80f80-156">تكلفة رسوم متنوعة</span><span class="sxs-lookup"><span data-stu-id="80f80-156">Header miscellaneous charge</span></span>
    - <span data-ttu-id="80f80-157">تكلفة الخط المتنوعة</span><span class="sxs-lookup"><span data-stu-id="80f80-157">Line miscellaneous charge</span></span>
    - <span data-ttu-id="80f80-158">إشعار دائن</span><span class="sxs-lookup"><span data-stu-id="80f80-158">Credit note</span></span>
    - <span data-ttu-id="80f80-159">أمر الإرجاع</span><span class="sxs-lookup"><span data-stu-id="80f80-159">Return order</span></span>
    - <span data-ttu-id="80f80-160">طلب الشراء</span><span class="sxs-lookup"><span data-stu-id="80f80-160">Purchase requisition</span></span>
    - <span data-ttu-id="80f80-161">مصاريف متنوعة لبند طلب الشراء</span><span class="sxs-lookup"><span data-stu-id="80f80-161">Purchase requisition line miscellaneous charge</span></span>
    - <span data-ttu-id="80f80-162">طلب عرض الأسعار</span><span class="sxs-lookup"><span data-stu-id="80f80-162">Request for quotation</span></span>
    - <span data-ttu-id="80f80-163">طلب مصاريف رأس عرض أسعار متنوعة</span><span class="sxs-lookup"><span data-stu-id="80f80-163">Request for quotation header miscellaneous charge</span></span>
    - <span data-ttu-id="80f80-164">طلب مصاريف بند عرض أسعار متنوعة</span><span class="sxs-lookup"><span data-stu-id="80f80-164">Request for quotation line miscellaneous charge</span></span>

- <span data-ttu-id="80f80-165">عملية المخزون</span><span class="sxs-lookup"><span data-stu-id="80f80-165">Inventory process</span></span>

    - <span data-ttu-id="80f80-166">أمر التحويل - الشحن</span><span class="sxs-lookup"><span data-stu-id="80f80-166">Transfer order – ship</span></span>
    - <span data-ttu-id="80f80-167">أمر التحويل - الاستلام</span><span class="sxs-lookup"><span data-stu-id="80f80-167">Transfer order – receive</span></span>

## <a name="related-resources"></a><span data-ttu-id="80f80-168">الموارد ذات الصلة</span><span class="sxs-lookup"><span data-stu-id="80f80-168">Related resources</span></span>

[<span data-ttu-id="80f80-169">بدء استخدام خدمة الضرائب</span><span class="sxs-lookup"><span data-stu-id="80f80-169">Get started with tax service</span></span>](./global-get-started-with-tax-calculation-service.md)

[<span data-ttu-id="80f80-170">رقم تسجيل ضريبة القيمة المضافة المتعدد</span><span class="sxs-lookup"><span data-stu-id="80f80-170">Multiple VAT registration number</span></span>](./emea-multiple-vat-registration-numbers.md)

[<span data-ttu-id="80f80-171">دعم ميزه الضريبة لأمر التحويل</span><span class="sxs-lookup"><span data-stu-id="80f80-171">Tax feature support for transfer order</span></span>](./tasks/tax-feature-support-for-transfer-order.md)

[<span data-ttu-id="80f80-172">كيفيه إنشاء ملحق في خدمة الضرائب</span><span class="sxs-lookup"><span data-stu-id="80f80-172">How to build extension in tax service</span></span>](./tax-service-add-data-fields-tax-integration-by-extension.md)