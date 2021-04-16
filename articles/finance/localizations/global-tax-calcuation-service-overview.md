---
title: خدمة حساب الضرائب (إصدار أولي)
description: يوضح هذا الموضوع النطاق الإجمالي والميزات الخاصة بخدمه حساب الضرائب.
author: wangchen
ms.date: 03/02/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: 518d3fda7b97e55d23beea6a1ba0e50b44a7aa0e
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/01/2021
ms.locfileid: "5818214"
---
# <a name="tax-calculation-service-preview"></a><span data-ttu-id="cfef7-103">خدمة حساب الضرائب (إصدار أولي)</span><span class="sxs-lookup"><span data-stu-id="cfef7-103">Tax calculation service (Preview)</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="cfef7-104">خدمة حساب الضريبة هي خدمة متعددة المستأجرين قابلة للتوسع بشكل كبير وتمكّن محرك الضرائب العالمي من أتمتة وتبسيط عملية تحديد الضرائب وحسابها.</span><span class="sxs-lookup"><span data-stu-id="cfef7-104">The tax calculation service is a hyper-scalable multitenant service that enables the global tax engine to automate and simplify the tax determination and calculation process.</span></span> <span data-ttu-id="cfef7-105">محرك الضرائب قابل للتكوين بالكامل.</span><span class="sxs-lookup"><span data-stu-id="cfef7-105">The tax engine is fully configurable.</span></span> <span data-ttu-id="cfef7-106">تتضمن العناصر التي يمكن تكوينها، على سبيل المثال لا الحصر، نموذج البيانات الخاضع للضريبة، وكود الضريبة، ومصفوفة تطبيق الضريبة، وصيغة حساب الضريبة.</span><span class="sxs-lookup"><span data-stu-id="cfef7-106">The elements that can be configured include, but aren't limited to, the taxable data model, tax code, tax applicability matrix, and tax calculation formula.</span></span> <span data-ttu-id="cfef7-107">يعمل محرك الضرائب على النظام الأساسي لخدمات Microsoft Azure الأساسية، ويقدم التكنولوجيا الحديثة وقابلية التوسع الأسي.</span><span class="sxs-lookup"><span data-stu-id="cfef7-107">The tax engine runs on the Microsoft Azure core services platform, and offers modern technology and exponential scalability.</span></span>

<span data-ttu-id="cfef7-108">تتكامل خدمه حساب الضرائب مع Dynamics 365 Finance وDynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="cfef7-108">The tax calculation service integrates with Dynamics 365 Finance and Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="cfef7-109">وأخيرُا، ستقوم أيضا بالتكامل مع Dynamics 365 Project Operations وDynamics 365 Commerce وتطبيقات أخرى تابعة للجهات الخارجية والجهات الأولى.</span><span class="sxs-lookup"><span data-stu-id="cfef7-109">Eventually, it will also integrate with Dynamics 365 Project Operations, Dynamics 365 Commerce, and other first-party and third-party applications.</span></span>

<span data-ttu-id="cfef7-110">خدمة حساب الضريبة هي محرك ضرائب قائم على Microsoft يوفر قابلية توسعة أسية.</span><span class="sxs-lookup"><span data-stu-id="cfef7-110">The tax calculation service is a Microsoft-based tax engine that offers exponential scalability.</span></span> <span data-ttu-id="cfef7-111">يمكن أن تساعدك في أداء المهام التالية:</span><span class="sxs-lookup"><span data-stu-id="cfef7-111">It can help you perform the following tasks:</span></span>

- <span data-ttu-id="cfef7-112">تكوين خدمة حساب الضريبة من خلال Regulatory Configuration Service (RCS).</span><span class="sxs-lookup"><span data-stu-id="cfef7-112">Configure the tax calculation service through Regulatory Configuration Service (RCS).</span></span> <span data-ttu-id="cfef7-113">إن RCS هي نسخة محسنة من مصمم التقارير الإلكترونية (ER) وهي متاح كخدمة قائمة بذاتها.</span><span class="sxs-lookup"><span data-stu-id="cfef7-113">RCS is an enhanced version of the Electronic reporting (ER) designer and is available as a standalone service.</span></span>
- <span data-ttu-id="cfef7-114">تكوين مصفوفة الضرائب لتحديد أكواد الضرائب ومعدلاتها تلقائيًا.</span><span class="sxs-lookup"><span data-stu-id="cfef7-114">Configure the tax matrix to automatically determine tax codes and rates.</span></span>
- <span data-ttu-id="cfef7-115">تكوين مصفوفة الضرائب لتحديد رقم التسجيل الضريبي تلقائيًا.</span><span class="sxs-lookup"><span data-stu-id="cfef7-115">Configure the tax matrix to automatically determine the tax registration number.</span></span>
- <span data-ttu-id="cfef7-116">تكوين مصمم حساب الضريبة لتحديد الصيغ والشروط.</span><span class="sxs-lookup"><span data-stu-id="cfef7-116">Configure the tax calculation designer to define formulas and conditions.</span></span>
- <span data-ttu-id="cfef7-117">مشاركة حل تحديد الضريبة وحسابها عبر الكيانات القانونية.</span><span class="sxs-lookup"><span data-stu-id="cfef7-117">Share the tax determination and calculation solution across legal entities.</span></span>

<span data-ttu-id="cfef7-118">لاستخدام خدمة حساب الضريبة، قم بتثبيت الوظيفة الإضافية لخدمة حساب الضريبة من مشروعك في Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="cfef7-118">To use the tax calculation service, install the tax calculation service add-in from your project in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="cfef7-119">ثم أكمل الإعداد في RCS، وقم بتمكين خدمة حساب الضريبة في Finance وSupply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="cfef7-119">Then complete the setup in RCS, and enable the tax calculation service in Finance and Supply Chain Management.</span></span> <span data-ttu-id="cfef7-120">لمزيد من المعلومات، راجع [بدء استخدام خدمة الضريبة](https://go.microsoft.com/fwlink/?linkid=2138482).</span><span class="sxs-lookup"><span data-stu-id="cfef7-120">For more information, see [Get started with tax service](https://go.microsoft.com/fwlink/?linkid=2138482).</span></span>

## <a name="availability"></a><span data-ttu-id="cfef7-121">التوفر</span><span class="sxs-lookup"><span data-stu-id="cfef7-121">Availability</span></span>

<span data-ttu-id="cfef7-122">خدمة حساب الضريبة متاحة فقط في بيئات آلية تحديد الصلاحيات ولعملاء محددين، من خلال برنامج المعاينة العامة.</span><span class="sxs-lookup"><span data-stu-id="cfef7-122">The tax calculation service is available only in sandbox environments and to selected customers, through a public preview program.</span></span> <span data-ttu-id="cfef7-123">في النهاية، ستصبح متاحة بشكل عام لجميع العملاء وفي بيئات الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="cfef7-123">Eventually, it will become generally available to all customers and in production environments.</span></span>

<span data-ttu-id="cfef7-124">سيستمر تقديم الميزات الجديدة في خدمة حساب الضريبة.</span><span class="sxs-lookup"><span data-stu-id="cfef7-124">New features will continue to be delivered in the tax calculation service.</span></span> <span data-ttu-id="cfef7-125">لذلك، تأكد من مراجعة أحدث الوثائق في كثير من الأحيان للتعرف على تغطية ونطاق الميزات المدعومة.</span><span class="sxs-lookup"><span data-stu-id="cfef7-125">Therefore, be sure to check the most up-to-date documentation often to learn about the coverage and scope of supported features.</span></span>

<span data-ttu-id="cfef7-126">يتم نشر خدمة حساب الضريبة في مناطق Azure الجغرافية التالية.</span><span class="sxs-lookup"><span data-stu-id="cfef7-126">The tax calculation service is deployed in the following Azure geographies.</span></span> <span data-ttu-id="cfef7-127">سيتم نشره أيضًا في المزيد من مناطق Azure الجغرافية، بناءً على احتياجات العملاء:</span><span class="sxs-lookup"><span data-stu-id="cfef7-127">It will also be deployed to more Azure geographies, based on customer needs:</span></span>

- <span data-ttu-id="cfef7-128">الولايات المتحدة</span><span class="sxs-lookup"><span data-stu-id="cfef7-128">United States</span></span>
- <span data-ttu-id="cfef7-129">أوروبا</span><span class="sxs-lookup"><span data-stu-id="cfef7-129">Europe</span></span>
- <span data-ttu-id="cfef7-130">فرنسا</span><span class="sxs-lookup"><span data-stu-id="cfef7-130">France</span></span>
- <span data-ttu-id="cfef7-131">المملكة المتحدة</span><span class="sxs-lookup"><span data-stu-id="cfef7-131">United Kingdom</span></span>

> [!NOTE]
> <span data-ttu-id="cfef7-132">لا تدعم خدمة حساب الضريبة عمليات النشر المحلية لـ Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="cfef7-132">The tax calculation service doesn't support on-premises deployments of Dynamics 365.</span></span> <span data-ttu-id="cfef7-133">كما أنه لا يدعم الإصدارات السابقة، مثل Dynamics AX 2012.</span><span class="sxs-lookup"><span data-stu-id="cfef7-133">It also doesn't support earlier versions, such as Dynamics AX 2012.</span></span>

## <a name="feature-highlights"></a><span data-ttu-id="cfef7-134">النقاط الرئيسية في الميزات</span><span class="sxs-lookup"><span data-stu-id="cfef7-134">Feature highlights</span></span>

- <span data-ttu-id="cfef7-135">مصفوفة ضرائب قابلة للتكوين لتحديد الضريبة وحسابها تلقائيًا</span><span class="sxs-lookup"><span data-stu-id="cfef7-135">A configurable tax matrix to automatically determine and calculate tax</span></span>
- <span data-ttu-id="cfef7-136">دعم لأرقام تسجيل ضريبة القيمة المضافة (VAT) المتعددة</span><span class="sxs-lookup"><span data-stu-id="cfef7-136">Support for multiple value-added tax (VAT) registration numbers</span></span>
- <span data-ttu-id="cfef7-137">دعم أمر التحويل لتحديد الضرائب وحسابها</span><span class="sxs-lookup"><span data-stu-id="cfef7-137">Transfer order support for tax determination and calculation</span></span>
- <span data-ttu-id="cfef7-138">دعم أمر التحويل لتحديد أرقام تسجيل متعددة لضريبة القيمة المضافة</span><span class="sxs-lookup"><span data-stu-id="cfef7-138">Transfer order support for determination of multiple VAT registration numbers</span></span>

## <a name="supported-transactions"></a><span data-ttu-id="cfef7-139">الحركات المدعومة</span><span class="sxs-lookup"><span data-stu-id="cfef7-139">Supported transactions</span></span>

<span data-ttu-id="cfef7-140">يمكن تمكين خدمة حساب الضريبة بواسطة الكيان القانوني والحركة.</span><span class="sxs-lookup"><span data-stu-id="cfef7-140">The tax calculation service can be enabled by legal entity and transaction.</span></span> <span data-ttu-id="cfef7-141">الحركات التالية مدعومة:</span><span class="sxs-lookup"><span data-stu-id="cfef7-141">The following transactions are supported:</span></span>

- <span data-ttu-id="cfef7-142">عملية المبيعات</span><span class="sxs-lookup"><span data-stu-id="cfef7-142">Sales process</span></span>

    - <span data-ttu-id="cfef7-143">عرض أسعار المبيعات</span><span class="sxs-lookup"><span data-stu-id="cfef7-143">Sales quotation</span></span>
    - <span data-ttu-id="cfef7-144">أمر مبيعات</span><span class="sxs-lookup"><span data-stu-id="cfef7-144">Sales order</span></span>
    - <span data-ttu-id="cfef7-145">التأكيد</span><span class="sxs-lookup"><span data-stu-id="cfef7-145">Confirmation</span></span>
    - <span data-ttu-id="cfef7-146">قائمة الانتقاء</span><span class="sxs-lookup"><span data-stu-id="cfef7-146">Picking list</span></span>
    - <span data-ttu-id="cfef7-147">إيصال التعبئة</span><span class="sxs-lookup"><span data-stu-id="cfef7-147">Packing slip</span></span>
    - <span data-ttu-id="cfef7-148">فاتورة المبيعات</span><span class="sxs-lookup"><span data-stu-id="cfef7-148">Sales invoice</span></span>
    - <span data-ttu-id="cfef7-149">إشعار دائن</span><span class="sxs-lookup"><span data-stu-id="cfef7-149">Credit note</span></span>
    - <span data-ttu-id="cfef7-150">أمر الإرجاع</span><span class="sxs-lookup"><span data-stu-id="cfef7-150">Return order</span></span>
    - <span data-ttu-id="cfef7-151">تكلفة رسوم متنوعة</span><span class="sxs-lookup"><span data-stu-id="cfef7-151">Header miscellaneous charge</span></span>
    - <span data-ttu-id="cfef7-152">تكلفة الخط المتنوعة</span><span class="sxs-lookup"><span data-stu-id="cfef7-152">Line miscellaneous charge</span></span>

- <span data-ttu-id="cfef7-153">عمليه الشراء</span><span class="sxs-lookup"><span data-stu-id="cfef7-153">Purchase process</span></span>

    - <span data-ttu-id="cfef7-154">أمر شراء</span><span class="sxs-lookup"><span data-stu-id="cfef7-154">Purchase order</span></span>
    - <span data-ttu-id="cfef7-155">التأكيد</span><span class="sxs-lookup"><span data-stu-id="cfef7-155">Confirmation</span></span>
    - <span data-ttu-id="cfef7-156">قائمة الإيصالات</span><span class="sxs-lookup"><span data-stu-id="cfef7-156">Receipts list</span></span>
    - <span data-ttu-id="cfef7-157">إيصال استلام المنتج</span><span class="sxs-lookup"><span data-stu-id="cfef7-157">Product receipt</span></span>
    - <span data-ttu-id="cfef7-158">فاتورة الشراء</span><span class="sxs-lookup"><span data-stu-id="cfef7-158">Purchase invoice</span></span>
    - <span data-ttu-id="cfef7-159">تكلفة رسوم متنوعة</span><span class="sxs-lookup"><span data-stu-id="cfef7-159">Header miscellaneous charge</span></span>
    - <span data-ttu-id="cfef7-160">تكلفة الخط المتنوعة</span><span class="sxs-lookup"><span data-stu-id="cfef7-160">Line miscellaneous charge</span></span>
    - <span data-ttu-id="cfef7-161">إشعار دائن</span><span class="sxs-lookup"><span data-stu-id="cfef7-161">Credit note</span></span>
    - <span data-ttu-id="cfef7-162">أمر الإرجاع</span><span class="sxs-lookup"><span data-stu-id="cfef7-162">Return order</span></span>
    - <span data-ttu-id="cfef7-163">طلب الشراء</span><span class="sxs-lookup"><span data-stu-id="cfef7-163">Purchase requisition</span></span>
    - <span data-ttu-id="cfef7-164">مصاريف متنوعة لبند طلب الشراء</span><span class="sxs-lookup"><span data-stu-id="cfef7-164">Purchase requisition line miscellaneous charge</span></span>
    - <span data-ttu-id="cfef7-165">طلب عرض الأسعار</span><span class="sxs-lookup"><span data-stu-id="cfef7-165">Request for quotation</span></span>
    - <span data-ttu-id="cfef7-166">طلب مصاريف رأس عرض أسعار متنوعة</span><span class="sxs-lookup"><span data-stu-id="cfef7-166">Request for quotation header miscellaneous charge</span></span>
    - <span data-ttu-id="cfef7-167">طلب مصاريف بند عرض أسعار متنوعة</span><span class="sxs-lookup"><span data-stu-id="cfef7-167">Request for quotation line miscellaneous charge</span></span>

- <span data-ttu-id="cfef7-168">عملية المخزون</span><span class="sxs-lookup"><span data-stu-id="cfef7-168">Inventory process</span></span>

    - <span data-ttu-id="cfef7-169">أمر التحويل - الشحن</span><span class="sxs-lookup"><span data-stu-id="cfef7-169">Transfer order – ship</span></span>
    - <span data-ttu-id="cfef7-170">أمر التحويل - الاستلام</span><span class="sxs-lookup"><span data-stu-id="cfef7-170">Transfer order – receive</span></span>

## <a name="related-resources"></a><span data-ttu-id="cfef7-171">الموارد ذات الصلة</span><span class="sxs-lookup"><span data-stu-id="cfef7-171">Related resources</span></span>

[<span data-ttu-id="cfef7-172">بدء استخدام خدمة الضرائب</span><span class="sxs-lookup"><span data-stu-id="cfef7-172">Get started with tax service</span></span>](https://go.microsoft.com/fwlink/?linkid=2138482)

[<span data-ttu-id="cfef7-173">رقم تسجيل ضريبة القيمة المضافة المتعدد</span><span class="sxs-lookup"><span data-stu-id="cfef7-173">Multiple VAT registration number</span></span>](https://go.microsoft.com/fwlink/?linkid=2153387)

[<span data-ttu-id="cfef7-174">دعم ميزه الضريبة لأمر التحويل</span><span class="sxs-lookup"><span data-stu-id="cfef7-174">Tax feature support for transfer order</span></span>](https://go.microsoft.com/fwlink/?linkid=2153388)

[<span data-ttu-id="cfef7-175">كيفيه إنشاء ملحق في خدمة الضرائب</span><span class="sxs-lookup"><span data-stu-id="cfef7-175">How to build extension in tax service</span></span>](https://go.microsoft.com/fwlink/?linkid=2138483)
