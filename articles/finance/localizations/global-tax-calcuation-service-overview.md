---
title: (إصدار أولي) حساب الضرائب
description: يوضح هذا الموضوع النطاق الإجمالي والميزات الخاصة بقدرة حساب الضريبة.
author: wangchen
ms.date: 06/03/2021
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
ms.openlocfilehash: 9daa6e001200d03a2639974fb6de618d77ddf09d
ms.sourcegitcommit: cb282e8d2306ab71adf80a84346a6863d2d019e8
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/03/2021
ms.locfileid: "6184091"
---
# <a name="tax-calculation-preview"></a><span data-ttu-id="cc5f7-103">(إصدار أولي) حساب الضرائب</span><span class="sxs-lookup"><span data-stu-id="cc5f7-103">Tax Calculation (Preview)</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="cc5f7-104">خدمة حساب الضريبة هي خدمة متعددة المستأجرين قابلة للتوسع بشكل كبير وتمكّن Global Tax Engine من أتمتة وتبسيط عملية تحديد الضرائب وحسابها.</span><span class="sxs-lookup"><span data-stu-id="cc5f7-104">Tax Calculation is a hyper-scalable multitenant service that enables the global tax engine to automate and simplify the tax determination and calculation process.</span></span> <span data-ttu-id="cc5f7-105">محرك الضرائب قابل للتكوين بالكامل.</span><span class="sxs-lookup"><span data-stu-id="cc5f7-105">The tax engine is fully configurable.</span></span> <span data-ttu-id="cc5f7-106">تتضمن العناصر التي يمكن تكوينها، على سبيل المثال لا الحصر، نموذج البيانات الخاضع للضريبة، وكود الضريبة، ومصفوفة تطبيق الضريبة، وصيغة حساب الضريبة.</span><span class="sxs-lookup"><span data-stu-id="cc5f7-106">The elements that can be configured include, but aren't limited to, the taxable data model, tax code, tax applicability matrix, and tax calculation formula.</span></span> <span data-ttu-id="cc5f7-107">يعمل محرك الضرائب على النظام الأساسي لخدمات Microsoft Azure الأساسية، ويقدم التكنولوجيا الحديثة وقابلية التوسع الأسي.</span><span class="sxs-lookup"><span data-stu-id="cc5f7-107">The tax engine runs on the Microsoft Azure core services platform, and offers modern technology and exponential scalability.</span></span>

<span data-ttu-id="cc5f7-108">تتكامل خدمه حساب الضريبة مع Dynamics 365 Finance وDynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="cc5f7-108">Tax Calculation integrates with Dynamics 365 Finance and Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="cc5f7-109">وأخيرُا، ستقوم أيضا بالتكامل مع Dynamics 365 Project Operations وDynamics 365 Commerce وتطبيقات أخرى تابعة للجهات الخارجية والجهات الأولى.</span><span class="sxs-lookup"><span data-stu-id="cc5f7-109">Eventually, it will also integrate with Dynamics 365 Project Operations, Dynamics 365 Commerce, and other first-party and third-party applications.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="cc5f7-110">عند تمكين ‏‫خدمة حساب الضرائب، قد يتم إجراء بعض العمليات على البيانات ذات الصلة في مركز بيانات غير مركز البيانات الذي يحتفظ ببيانات الخدمة الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="cc5f7-110">When you enable the Tax Calculation service, some operations on related data might be performed in a data center other than the data center that maintains your service data.</span></span> <span data-ttu-id="cc5f7-111">راجع [الشروط والأحكام](../../fin-ops-core/fin-ops/get-started/public-preview-terms.md) قبل تمكين خدمة حساب الضرائب.</span><span class="sxs-lookup"><span data-stu-id="cc5f7-111">Review the [Terms and Conditions](../../fin-ops-core/fin-ops/get-started/public-preview-terms.md) before you enable the Tax Calculation service.</span></span> <span data-ttu-id="cc5f7-112">خصوصيتك تهمنا.</span><span class="sxs-lookup"><span data-stu-id="cc5f7-112">Your privacy is important to us.</span></span> <span data-ttu-id="cc5f7-113">لمعرفه المزيد، اقرأ [بيان الخصوصية](https://go.microsoft.com/fwlink/?LinkId=521839).</span><span class="sxs-lookup"><span data-stu-id="cc5f7-113">To learn more, read our [Privacy Statement](https://go.microsoft.com/fwlink/?LinkId=521839).</span></span>

<span data-ttu-id="cc5f7-114">خدمة حساب الضريبة هي محرك ضرائب قائم على الخدمات الصغيرة يوفر قابلية توسعة أسية.</span><span class="sxs-lookup"><span data-stu-id="cc5f7-114">Tax Calculation is a microservice-based tax engine that offers exponential scalability.</span></span> <span data-ttu-id="cc5f7-115">يمكن أن تساعدك في أداء المهام التالية:</span><span class="sxs-lookup"><span data-stu-id="cc5f7-115">It can help you perform the following tasks:</span></span>

- <span data-ttu-id="cc5f7-116">تكوين حساب الضريبة من خلال Regulatory Configuration Service (RCS).</span><span class="sxs-lookup"><span data-stu-id="cc5f7-116">Configure Tax Calculation through Regulatory Configuration Service (RCS).</span></span> <span data-ttu-id="cc5f7-117">إن RCS هي نسخة محسنة من مصمم التقارير الإلكترونية (ER) وهي متاح كخدمة قائمة بذاتها.</span><span class="sxs-lookup"><span data-stu-id="cc5f7-117">RCS is an enhanced version of the Electronic reporting (ER) designer and is available as a standalone service.</span></span>
- <span data-ttu-id="cc5f7-118">تكوين مصفوفة الضرائب لتحديد أكواد الضرائب ومعدلاتها تلقائيًا.</span><span class="sxs-lookup"><span data-stu-id="cc5f7-118">Configure the tax matrix to automatically determine tax codes and rates.</span></span>
- <span data-ttu-id="cc5f7-119">تكوين مصفوفة الضرائب لتحديد رقم التسجيل الضريبي تلقائيًا.</span><span class="sxs-lookup"><span data-stu-id="cc5f7-119">Configure the tax matrix to automatically determine the tax registration number.</span></span>
- <span data-ttu-id="cc5f7-120">تكوين مصمم حساب الضريبة لتحديد الصيغ والشروط.</span><span class="sxs-lookup"><span data-stu-id="cc5f7-120">Configure the tax calculation designer to define formulas and conditions.</span></span>
- <span data-ttu-id="cc5f7-121">مشاركة حل تحديد الضريبة وحسابها عبر الكيانات القانونية.</span><span class="sxs-lookup"><span data-stu-id="cc5f7-121">Share the tax determination and calculation solution across legal entities.</span></span>

<span data-ttu-id="cc5f7-122">لاستخدام خدمة حساب الضريبة، قم بتثبيت الوظيفة الإضافية لخدمة حساب الضريبة من مشروعك في Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="cc5f7-122">To use the tax calculation service, install the tax calculation service add-in from your project in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="cc5f7-123">ثم أكمل الإعداد في RCS، وقم بتمكين خدمة حساب الضريبة في Finance وSupply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="cc5f7-123">Then complete the setup in RCS, and enable the tax calculation service in Finance and Supply Chain Management.</span></span> <span data-ttu-id="cc5f7-124">لمزيد من المعلومات، راجع [بدء استخدام خدمة الضريبة](./global-get-started-with-tax-calculation-service.md).</span><span class="sxs-lookup"><span data-stu-id="cc5f7-124">For more information, see [Get started with tax service](./global-get-started-with-tax-calculation-service.md).</span></span>

## <a name="availability"></a><span data-ttu-id="cc5f7-125">التوفر</span><span class="sxs-lookup"><span data-stu-id="cc5f7-125">Availability</span></span>

<span data-ttu-id="cc5f7-126">خدمة حساب الضريبة متاحة فقط في بيئات آلية تحديد الصلاحيات ولعملاء محددين، من خلال برنامج الإصدار الأولي.</span><span class="sxs-lookup"><span data-stu-id="cc5f7-126">Tax Calculation is available only in sandbox environments and to selected customers, through a public preview program.</span></span> <span data-ttu-id="cc5f7-127">في النهاية، ستصبح متاحة بشكل عام لجميع العملاء وفي بيئات الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="cc5f7-127">Eventually, it will become generally available to all customers and in production environments.</span></span>

<span data-ttu-id="cc5f7-128">سيستمر تسليم الميزات الجديدة، لذا تأكد من مراجعة أحدث الوثائق في كثير من الأحيان للتعرف على تغطية ونطاق الميزات المدعومة.</span><span class="sxs-lookup"><span data-stu-id="cc5f7-128">New features will continue to be delivered, so be sure to check the most up-to-date documentation often to learn about the coverage and scope of supported features.</span></span>

<span data-ttu-id="cc5f7-129">يتم نشر خدمة حساب الضريبة في مناطق Azure الجغرافية التالية.</span><span class="sxs-lookup"><span data-stu-id="cc5f7-129">Tax Calculation is deployed in the following Azure geographies.</span></span> <span data-ttu-id="cc5f7-130">سيتم نشره أيضًا في المزيد من مناطق Azure الجغرافية، بناءً على احتياجات العملاء:</span><span class="sxs-lookup"><span data-stu-id="cc5f7-130">It will also be deployed to more Azure geographies, based on customer needs:</span></span>

- <span data-ttu-id="cc5f7-131">الولايات المتحدة</span><span class="sxs-lookup"><span data-stu-id="cc5f7-131">United States</span></span>
- <span data-ttu-id="cc5f7-132">أوروبا</span><span class="sxs-lookup"><span data-stu-id="cc5f7-132">Europe</span></span>

> [!NOTE]
> <span data-ttu-id="cc5f7-133">لا تدعم خدمة حساب الضريبة عمليات النشر المحلية لـ Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="cc5f7-133">Tax Calculation doesn't support on-premises deployments of Dynamics 365.</span></span> <span data-ttu-id="cc5f7-134">كما أنه لا يدعم الإصدارات السابقة، مثل Dynamics AX 2012.</span><span class="sxs-lookup"><span data-stu-id="cc5f7-134">It also doesn't support earlier versions, such as Dynamics AX 2012.</span></span>

## <a name="feature-highlights"></a><span data-ttu-id="cc5f7-135">النقاط الرئيسية في الميزات</span><span class="sxs-lookup"><span data-stu-id="cc5f7-135">Feature highlights</span></span>

- <span data-ttu-id="cc5f7-136">مصفوفة ضرائب قابلة للتكوين لتحديد الضريبة وحسابها تلقائيًا</span><span class="sxs-lookup"><span data-stu-id="cc5f7-136">A configurable tax matrix to automatically determine and calculate tax</span></span>
- <span data-ttu-id="cc5f7-137">دعم لأرقام تسجيل الضريبة المتعددة</span><span class="sxs-lookup"><span data-stu-id="cc5f7-137">Support for multiple tax registration numbers</span></span>
- <span data-ttu-id="cc5f7-138">دعم أمر التحويل لتحديد الضرائب وحسابها</span><span class="sxs-lookup"><span data-stu-id="cc5f7-138">Transfer order support for tax determination and calculation</span></span>
- <span data-ttu-id="cc5f7-139">دعم أمر التحويل لتحديد أرقام تسجيل متعددة للضريبة</span><span class="sxs-lookup"><span data-stu-id="cc5f7-139">Transfer order support for determination of multiple tax registration numbers</span></span>

## <a name="supported-transactions"></a><span data-ttu-id="cc5f7-140">الحركات المدعومة</span><span class="sxs-lookup"><span data-stu-id="cc5f7-140">Supported transactions</span></span>

<span data-ttu-id="cc5f7-141">يمكن تمكين خدمة حساب الضريبة بواسطة الكيان القانوني والحركة.</span><span class="sxs-lookup"><span data-stu-id="cc5f7-141">Tax Calculation can be enabled by legal entity and transaction.</span></span> <span data-ttu-id="cc5f7-142">الحركات التالية مدعومة:</span><span class="sxs-lookup"><span data-stu-id="cc5f7-142">The following transactions are supported:</span></span>

- <span data-ttu-id="cc5f7-143">عملية المبيعات</span><span class="sxs-lookup"><span data-stu-id="cc5f7-143">Sales process</span></span>

    - <span data-ttu-id="cc5f7-144">عرض أسعار المبيعات</span><span class="sxs-lookup"><span data-stu-id="cc5f7-144">Sales quotation</span></span>
    - <span data-ttu-id="cc5f7-145">أمر مبيعات</span><span class="sxs-lookup"><span data-stu-id="cc5f7-145">Sales order</span></span>
    - <span data-ttu-id="cc5f7-146">التأكيد</span><span class="sxs-lookup"><span data-stu-id="cc5f7-146">Confirmation</span></span>
    - <span data-ttu-id="cc5f7-147">قائمة الانتقاء</span><span class="sxs-lookup"><span data-stu-id="cc5f7-147">Picking list</span></span>
    - <span data-ttu-id="cc5f7-148">إيصال التعبئة</span><span class="sxs-lookup"><span data-stu-id="cc5f7-148">Packing slip</span></span>
    - <span data-ttu-id="cc5f7-149">فاتورة المبيعات</span><span class="sxs-lookup"><span data-stu-id="cc5f7-149">Sales invoice</span></span>
    - <span data-ttu-id="cc5f7-150">إشعار دائن</span><span class="sxs-lookup"><span data-stu-id="cc5f7-150">Credit note</span></span>
    - <span data-ttu-id="cc5f7-151">أمر الإرجاع</span><span class="sxs-lookup"><span data-stu-id="cc5f7-151">Return order</span></span>
    - <span data-ttu-id="cc5f7-152">تكلفة رسوم متنوعة</span><span class="sxs-lookup"><span data-stu-id="cc5f7-152">Header miscellaneous charge</span></span>
    - <span data-ttu-id="cc5f7-153">تكلفة الخط المتنوعة</span><span class="sxs-lookup"><span data-stu-id="cc5f7-153">Line miscellaneous charge</span></span>

- <span data-ttu-id="cc5f7-154">عمليه الشراء</span><span class="sxs-lookup"><span data-stu-id="cc5f7-154">Purchase process</span></span>

    - <span data-ttu-id="cc5f7-155">أمر شراء</span><span class="sxs-lookup"><span data-stu-id="cc5f7-155">Purchase order</span></span>
    - <span data-ttu-id="cc5f7-156">التأكيد</span><span class="sxs-lookup"><span data-stu-id="cc5f7-156">Confirmation</span></span>
    - <span data-ttu-id="cc5f7-157">قائمة الإيصالات</span><span class="sxs-lookup"><span data-stu-id="cc5f7-157">Receipts list</span></span>
    - <span data-ttu-id="cc5f7-158">إيصال استلام المنتج</span><span class="sxs-lookup"><span data-stu-id="cc5f7-158">Product receipt</span></span>
    - <span data-ttu-id="cc5f7-159">فاتورة الشراء</span><span class="sxs-lookup"><span data-stu-id="cc5f7-159">Purchase invoice</span></span>
    - <span data-ttu-id="cc5f7-160">تكلفة رسوم متنوعة</span><span class="sxs-lookup"><span data-stu-id="cc5f7-160">Header miscellaneous charge</span></span>
    - <span data-ttu-id="cc5f7-161">تكلفة الخط المتنوعة</span><span class="sxs-lookup"><span data-stu-id="cc5f7-161">Line miscellaneous charge</span></span>
    - <span data-ttu-id="cc5f7-162">إشعار دائن</span><span class="sxs-lookup"><span data-stu-id="cc5f7-162">Credit note</span></span>
    - <span data-ttu-id="cc5f7-163">أمر الإرجاع</span><span class="sxs-lookup"><span data-stu-id="cc5f7-163">Return order</span></span>
    - <span data-ttu-id="cc5f7-164">طلب الشراء</span><span class="sxs-lookup"><span data-stu-id="cc5f7-164">Purchase requisition</span></span>
    - <span data-ttu-id="cc5f7-165">مصاريف متنوعة لبند طلب الشراء</span><span class="sxs-lookup"><span data-stu-id="cc5f7-165">Purchase requisition line miscellaneous charge</span></span>
    - <span data-ttu-id="cc5f7-166">طلب عرض الأسعار</span><span class="sxs-lookup"><span data-stu-id="cc5f7-166">Request for quotation</span></span>
    - <span data-ttu-id="cc5f7-167">طلب مصاريف رأس عرض أسعار متنوعة</span><span class="sxs-lookup"><span data-stu-id="cc5f7-167">Request for quotation header miscellaneous charge</span></span>
    - <span data-ttu-id="cc5f7-168">طلب مصاريف بند عرض أسعار متنوعة</span><span class="sxs-lookup"><span data-stu-id="cc5f7-168">Request for quotation line miscellaneous charge</span></span>

- <span data-ttu-id="cc5f7-169">عملية المخزون</span><span class="sxs-lookup"><span data-stu-id="cc5f7-169">Inventory process</span></span>

    - <span data-ttu-id="cc5f7-170">أمر التحويل - الشحن</span><span class="sxs-lookup"><span data-stu-id="cc5f7-170">Transfer order – ship</span></span>
    - <span data-ttu-id="cc5f7-171">أمر التحويل - الاستلام</span><span class="sxs-lookup"><span data-stu-id="cc5f7-171">Transfer order – receive</span></span>

## <a name="related-resources"></a><span data-ttu-id="cc5f7-172">الموارد ذات الصلة</span><span class="sxs-lookup"><span data-stu-id="cc5f7-172">Related resources</span></span>

[<span data-ttu-id="cc5f7-173">بدء استخدام خدمة الضرائب</span><span class="sxs-lookup"><span data-stu-id="cc5f7-173">Get started with tax service</span></span>](./global-get-started-with-tax-calculation-service.md)

[<span data-ttu-id="cc5f7-174">رقم تسجيل ضريبة القيمة المضافة المتعدد</span><span class="sxs-lookup"><span data-stu-id="cc5f7-174">Multiple VAT registration number</span></span>](./emea-multiple-vat-registration-numbers.md)

[<span data-ttu-id="cc5f7-175">دعم ميزه الضريبة لأمر التحويل</span><span class="sxs-lookup"><span data-stu-id="cc5f7-175">Tax feature support for transfer order</span></span>](./tasks/tax-feature-support-for-transfer-order.md)

[<span data-ttu-id="cc5f7-176">كيفيه إنشاء ملحق في خدمة الضرائب</span><span class="sxs-lookup"><span data-stu-id="cc5f7-176">How to build extension in tax service</span></span>](./tax-service-add-data-fields-tax-integration-by-extension.md)
