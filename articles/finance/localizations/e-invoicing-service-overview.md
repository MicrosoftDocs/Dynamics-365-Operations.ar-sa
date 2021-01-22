---
title: نظرة عامة على الوظيفة الإضافية الفوترة الإلكترونية
description: يوفر هذا الموضوع معلومات حول الوظيفة الإضافية الفوترة الإلكترونية في Microsoft Dynamics 365 Finance وفي Dynamics 365 Supply Chain Management.
author: gionoder
manager: AnnBe
ms.date: 09/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: ffd48e173b66cc6d2571e666d5452a5eff05176c
ms.sourcegitcommit: d6250ee5ced43be39e789324a895fd1c07178935
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/19/2020
ms.locfileid: "4039736"
---
# <a name="electronic-invoicing-add-on-overview"></a><span data-ttu-id="fa184-103">نظرة عامة على الوظيفة الإضافية الفوترة الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="fa184-103">Electronic invoicing add-on overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fa184-104">تُعد الوظيفة الإضافية الفوترة الإلكترونية لكل من Microsoft Dynamics 365 Finance وDynamics 365 Supply Chain Management خدمة متعددة المستأجرين قابلة للتوسعة بشكل كبير. وهي تمكّن المعالجة القابلة للتكوين لمستندات الفواتير الإلكترونية ومبادلة المستندات القابلة للتكوين.</span><span class="sxs-lookup"><span data-stu-id="fa184-104">The Electronic invoicing add-on for Microsoft Dynamics 365 Finance and Dynamics 365 Supply Chain Management is a hyper-scalable multitenant service that enables configurable processing of electronic invoice documents and configurable document exchange.</span></span> <span data-ttu-id="fa184-105">قواعد المعالجة والتكامل قابلة للتكوين بشكل كامل، ويتم تشغيل المنطق خارج Finance وSupply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="fa184-105">The processing and integration rules are fully configurable, and the logic is run outside Finance and Supply Chain Management.</span></span> <span data-ttu-id="fa184-106">تستهدف الخدمة بشكل أساسي معالجة الفواتير الإلكترونية في سيناريوهات الأعمال إلى الحكومة، ولكن يمكن تكوينها بشكل مخصص لأغراض أخرى.</span><span class="sxs-lookup"><span data-stu-id="fa184-106">The service is targeted mainly at e-invoice processing in business-to-government scenarios, but it can be custom-configured for other purposes.</span></span>

<span data-ttu-id="fa184-107">بإمكان الوظيفة الإضافية الفوترة الإلكترونية أن تساعدك على تحقيق الأهداف التالية:</span><span class="sxs-lookup"><span data-stu-id="fa184-107">The Electronic invoicing add-on can help you achieve the following goals:</span></span>

- <span data-ttu-id="fa184-108">اعتماد سريع وسهل للمتطلبات الخاصة بالبلدان/المناطق</span><span class="sxs-lookup"><span data-stu-id="fa184-108">Fast and easy adoption of country/region-specific requirements</span></span>
- <span data-ttu-id="fa184-109">عمليات تنفيذ موحدة لحل الوظيفة الإضافية الفوترة الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="fa184-109">Standardized implementations of an Electronic invoicing add-on solution</span></span>
- <span data-ttu-id="fa184-110">إمكانية تتبع محسنة لمحفوظات المستندات</span><span class="sxs-lookup"><span data-stu-id="fa184-110">Enhanced traceability of document history</span></span>
- <span data-ttu-id="fa184-111">دورة تنفيذ أقصر</span><span class="sxs-lookup"><span data-stu-id="fa184-111">Shorter implementation cycle</span></span>
- <span data-ttu-id="fa184-112">إجمالي تكلفة ملكية منخفضة (TCO)</span><span class="sxs-lookup"><span data-stu-id="fa184-112">Reduced total cost of ownership (TCO)</span></span>
- <span data-ttu-id="fa184-113">تكوينات سهله التعديل لا تتطلب تغييرات في التعليمات البرمجية</span><span class="sxs-lookup"><span data-stu-id="fa184-113">Easily adjustable configurations that don't required code changes</span></span>
- <span data-ttu-id="fa184-114">إنشاء حزم تكوين بشكل مبسّط</span><span class="sxs-lookup"><span data-stu-id="fa184-114">Simplified configuration packaging</span></span>
- <span data-ttu-id="fa184-115">عمليات تصدير واستيراد وتكامل مضمنة، وقابلية توسعة سهلة في معالجة مستندات الفواتير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="fa184-115">Built-in export, import, and integration, and easy extensibility in the processing of e-invoice documents</span></span>
- <span data-ttu-id="fa184-116">سهولة إعادة استخدام تكوينات التصدير والاستيراد والتكامل عبر الشركات.</span><span class="sxs-lookup"><span data-stu-id="fa184-116">Easy reuse of the same export, import, and integration configurations across companies</span></span>

<span data-ttu-id="fa184-117">لاستخدام الوظيفة الإضافية الفوترة الإلكتروني، يجب تثبيتها من المشروع في Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="fa184-117">To use the Electronic invoicing add-on, you must install it from your project in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="fa184-118">بعد ذلك، اتبع إجراء الإعداد لتشغيل التكامل مع Finance أو Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="fa184-118">Next, follow the setup procedure to turn on the integration with Finance or Supply Chain Management.</span></span> <span data-ttu-id="fa184-119">لمزيد من المعلومات، راجع [بدء استخدام الوظيفة الإضافية الفوترة الإلكترونية](e-invoicing-get-started.md).</span><span class="sxs-lookup"><span data-stu-id="fa184-119">For more information, see [Get started with the Electronic invoicing add-on](e-invoicing-get-started.md).</span></span>

## <a name="availability"></a><span data-ttu-id="fa184-120">التوفر</span><span class="sxs-lookup"><span data-stu-id="fa184-120">Availability</span></span>

<span data-ttu-id="fa184-121">بشكل مبدئي، تتوفر الوظيفة الإضافية الفوترة الإلكترونية للعملاء المحددين من خلال برنامج معاينة.</span><span class="sxs-lookup"><span data-stu-id="fa184-121">Initially, the Electronic invoicing add-on is available to selected customers through a preview program.</span></span> <span data-ttu-id="fa184-122">في وقت لاحق، يتم فتح المعاينة إلى نطاق أوسع من العملاء.</span><span class="sxs-lookup"><span data-stu-id="fa184-122">Later, the preview will be opened to a wider range of customers.</span></span> <span data-ttu-id="fa184-123">أخيرًا، ستصبح الخدمة متوفرة بشكل عام.</span><span class="sxs-lookup"><span data-stu-id="fa184-123">Finally, the service will become generally available.</span></span> <span data-ttu-id="fa184-124">لأن الوظيفة التي تقوم بمعالجة المتطلبات الخاصة بالبلدان/المناطق قد تكون محدودة في مراحل مختلفة من الإصدار، يجب عليك دائمًا التحقق من الوثائق الحديثة التي تلقي الضوء على تغطية ونطاق الحلول الخاصة بالبلدان/المناطق.</span><span class="sxs-lookup"><span data-stu-id="fa184-124">Because functionality that addresses country/region-specific requirements might be limited at different phases of the release, you should always check the most up-to-date documentation that highlights the coverage and scope of supported country/region-specific solutions.</span></span>

<span data-ttu-id="fa184-125">يتم نشر الوظيفة الإضافية الفوترة الإلكترونية في مناطق Azure الجغرافية التالية:</span><span class="sxs-lookup"><span data-stu-id="fa184-125">The Electronic invoicing add-on is deployed in the following Azure geographies:</span></span>

- <span data-ttu-id="fa184-126">الولايات المتحدة</span><span class="sxs-lookup"><span data-stu-id="fa184-126">United States</span></span>
- <span data-ttu-id="fa184-127">أوروبا</span><span class="sxs-lookup"><span data-stu-id="fa184-127">Europe</span></span>

> [!NOTE]
> <span data-ttu-id="fa184-128">لا تدعم الوظيفة الإضافة الفوترة الإلكترونية عمليات النشر المحلية.</span><span class="sxs-lookup"><span data-stu-id="fa184-128">The Electronic invoicing add-on doesn't support on-premises deployments.</span></span>

## <a name="extended-configurability"></a><span data-ttu-id="fa184-129">قابلية تكوين موسعة</span><span class="sxs-lookup"><span data-stu-id="fa184-129">Extended configurability</span></span>

<span data-ttu-id="fa184-130">يمكن استخدام الوظيفة الإضافية الفوترة الإلكترونية في السيناريوهات حيث يجب عليك إنشاء مستند الكتروني وإرساله إلى الأطراف المعينة.</span><span class="sxs-lookup"><span data-stu-id="fa184-130">The Electronic invoicing add-on can be used in scenarios where you must create and send an electronic document to the designated parties.</span></span> <span data-ttu-id="fa184-131">لقد تم تصميمها خصيصًا لتشغيل سير مهام قابل للتكوين من إجراءات المعالجة، استنادًا إلى البيانات المستلمة.</span><span class="sxs-lookup"><span data-stu-id="fa184-131">It's specifically designed for running a configurable flow of processing actions, based on received data.</span></span> <span data-ttu-id="fa184-132">تقتصر خيارات قابلية التكوين المتوفرة في Finance وSupply Chain Management على تحويل المستندات.</span><span class="sxs-lookup"><span data-stu-id="fa184-132">The configurability options that are available in Finance and Supply Chain Management are limited to document transformation.</span></span> <span data-ttu-id="fa184-133">تقوم الخدمة بتوسيع هذه الخيارات عن طريق إضافة عمليات تكامل قابلة للتكوين متوفرة فيها.</span><span class="sxs-lookup"><span data-stu-id="fa184-133">The service extends these options by adding the configurable integrations that are available in it.</span></span> <span data-ttu-id="fa184-134">علاوةً على ذلك، فإن جميع وظائف الفواتير الإلكترونية التي كانت متوفرة في وقت سابق، مثل Brazilian Nota fiscal eletrônica (NF-e) أو Mexican Comprobante Fiscal Digital por Internet (CFDI) أو لغة الأعمال العامة (UBL) لأوروبا الشرقية/Pan-European Public Procurement OnLine (PEPPOL)، ستستخدم تكوينات التصدير والاستيراد، ولتمكين التكامل مع خدمات الويب الخارجية.</span><span class="sxs-lookup"><span data-stu-id="fa184-134">In addition, all the electronic invoice functionalities that were previously available, such as Brazilian Nota fiscal eletrônica (NF-e), Mexican Comprobante Fiscal Digital por Internet (CFDI), or other Western European Universal Business Language (UBL)/Pan-European Public Procurement OnLine (PEPPOL) functionalities, will use configurations for export and import, and to enable integrations with external web services.</span></span>

## <a name="feature-highlights"></a><span data-ttu-id="fa184-135">النقاط الرئيسية في الميزات</span><span class="sxs-lookup"><span data-stu-id="fa184-135">Feature highlights</span></span>

- <span data-ttu-id="fa184-136">تكامل جاهز مع Finance وSupply Chain Management</span><span class="sxs-lookup"><span data-stu-id="fa184-136">Out-of-box integration with Finance and Supply Chain management</span></span>
- <span data-ttu-id="fa184-137">تجربة مستخدم متسقة لتكوين ومراقبة عملية الفاتورة الإلكترونية لجميع البلدان أو المناطق</span><span class="sxs-lookup"><span data-stu-id="fa184-137">Consistent user experience for the configuration and monitoring of the e-invoice process for all countries or regions</span></span>
- <span data-ttu-id="fa184-138">اعتماد أسهل وأسرع وأقل تكلفة لحلول الفوترة الإلكترونية في بلدان أو مناطق جديدة</span><span class="sxs-lookup"><span data-stu-id="fa184-138">Faster, easier, and less expensive adoption of Electronic invoicing add-on solutions in new countries or regions</span></span>
- <span data-ttu-id="fa184-139">تكوين الخدمة من خلال Regulatory Configuration Services (RCS) وإعداد ميزة العولمة.</span><span class="sxs-lookup"><span data-stu-id="fa184-139">Configuration of the service through the Regulatory Configuration Service (RCS) and Globalization feature setup</span></span>
- <span data-ttu-id="fa184-140">تحويل بيانات العمل إلى تنسيقات الفواتير الإلكترونية المتعددة (XML وJavaScript Object Notation \[JSON\] وTXT والقيم المفصولة بفواصل \[CSV\]) باستخدام التكوينات المعرّفة في RCS:</span><span class="sxs-lookup"><span data-stu-id="fa184-140">Transformation of business data into multiple e-invoice formats (XML, JavaScript Object Notation \[JSON\], TXT, and comma-separated values \[CSV\]) by using configurations that are defined in RCS:</span></span>

    - <span data-ttu-id="fa184-141">تنسيقات التقارير الإلكترونية المتاحة للبلدان أو المناطق التي لا تتوفر فيها عملية تحويل الفاتورة الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="fa184-141">Electronic reporting formats that are available for countries or regions where configurability for e-invoice transformation isn't available</span></span>

- <span data-ttu-id="fa184-142">الإرسال القابل للتكوين للفواتير الإلكترونية إلى خدمات الويب الخارجية، بما في ذلك معالجة الشهادة من خلال التوقيعات الرقمية:</span><span class="sxs-lookup"><span data-stu-id="fa184-142">Configurable submission of e-invoices to external web services, including certification handling through digital signatures:</span></span>

    - <span data-ttu-id="fa184-143">تكامل مدمج وسهل التوسعة وقابل للتكوين مع محتوى إضافي لبلدان متعددة</span><span class="sxs-lookup"><span data-stu-id="fa184-143">Built-in, easily extendable, and configurable integration with additional content for several countries</span></span>

    > [!NOTE]
    > <span data-ttu-id="fa184-144">في الوقت الحالي، هناك عدد محدود مدعوم من عمليات الإرسال المباشرة.</span><span class="sxs-lookup"><span data-stu-id="fa184-144">Currently, a limited number of direct submissions are supported.</span></span> <span data-ttu-id="fa184-145">لمزيد من المعلومات، راجع القسم [التوفر](#availability) سابقًا في هذا الموضوع.</span><span class="sxs-lookup"><span data-stu-id="fa184-145">For more information, see the [Availability](#availability) section earlier in this topic.</span></span> <span data-ttu-id="fa184-146">سيتم تقديم الدعم في المستقبل.</span><span class="sxs-lookup"><span data-stu-id="fa184-146">Support will be extended in the future.</span></span>

- <span data-ttu-id="fa184-147">معالجة الاستجابات من خدمات الويب، بما في ذلك معالجة رسالة الاستثناء القابلة للتكوين</span><span class="sxs-lookup"><span data-stu-id="fa184-147">Handling of responses from web services, including configurable exception message handling</span></span>
- <span data-ttu-id="fa184-148">دعم التوقيعات الإلكترونية (على سبيل المثال، باستخدام خوارزمية التوقيع XMLDSig)</span><span class="sxs-lookup"><span data-stu-id="fa184-148">Support for electronic signatures (for example, by using the XMLDSig signing algorithm)</span></span>
- <span data-ttu-id="fa184-149">المعالجة الدُفعية لرسائل الفاتورة الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="fa184-149">Batch processing of e-invoice messages</span></span>

## <a name="architecture-and-data-flow"></a><span data-ttu-id="fa184-150">البنية وتدفق البيانات</span><span class="sxs-lookup"><span data-stu-id="fa184-150">Architecture and data flow</span></span>

<span data-ttu-id="fa184-151">عندما يتم تثبيت الوظيفة الإضافية الفوترة الإلكترونية من LCS، وتم إكمال الإعداد المطلوب في كافة التطبيقات المطلوبة، يتم تأسيس اتصال آمن.</span><span class="sxs-lookup"><span data-stu-id="fa184-151">When the Electronic invoicing add-on is installed from LCS, and the required setup is completed in all required applications, a secure connection is established.</span></span> <span data-ttu-id="fa184-152">توجد الخدمة حاليًا في مراكز البيانات في الولايات المتحدة وأوروبا.</span><span class="sxs-lookup"><span data-stu-id="fa184-152">The service is currently located in data centers in the United States and Europe.</span></span> <span data-ttu-id="fa184-153">وبالتالي، قد يختلف موقع الخدمة عن موقع مثيل Finance أو Supply Chain Management المرتبط.</span><span class="sxs-lookup"><span data-stu-id="fa184-153">Therefore, the service location might differ from the location of the related Finance or Supply Chain Management instance.</span></span> <span data-ttu-id="fa184-154">بعد إكمال إعداد الوظيفة الإضافية الفوترة الإلكترونية وتشغيل التكامل، وكلما تم إرسال فاتورة إلكترونية، يتم إرسال البيانات الرئيسية وبيانات المعاملات المرتبطة بمستند معين إلى الوظيفة الإضافية الفوترة الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="fa184-154">After you complete the setup of the Electronic invoicing add-on and turn on the integration, whenever an electronic invoice is sent, master data and transactional data that are related to a specific document are sent to the Electronic invoicing add-on.</span></span>

> [!NOTE]
> <span data-ttu-id="fa184-155">إذا احتوت فاتورتك الإلكترونية أو أي مستند آخر على بيانات شخصية، تأكد من أن استخدامك لهذه الميزة يلبي القانون العام لحماية البيانات (GDPR) واللوائح الأخرى المرتبطة بنقل البيانات الشخصية.</span><span class="sxs-lookup"><span data-stu-id="fa184-155">If your electronic invoice or any other document contains personal data, verify that your use of this feature meets the General Data Protection Regulation (GDPR) and other regulations that are related to the transfer of personal data.</span></span>

### <a name="high-level-description-of-the-data-flow"></a><span data-ttu-id="fa184-156">وصف عالي المستوي لتدفق البيانات</span><span class="sxs-lookup"><span data-stu-id="fa184-156">High-level description of the data flow</span></span>

1. <span data-ttu-id="fa184-157">يقوم العميل بإرسال مستند أعمال متعارف عليه إلى الخدمة.</span><span class="sxs-lookup"><span data-stu-id="fa184-157">The client sends a canonical business document to the service.</span></span>
2. <span data-ttu-id="fa184-158">استنادًا إلى معلومات السياق التي يتم تلقيها من العميل، تحدد الخدمة سير مهام المعالجة القابل للتطبيق.</span><span class="sxs-lookup"><span data-stu-id="fa184-158">Based on the context information that is received from the client, the service selects the applicable processing flow.</span></span>
3. <span data-ttu-id="fa184-159">تعمل الخدمة على تشغيل إجراءات المعالجة.</span><span class="sxs-lookup"><span data-stu-id="fa184-159">The service runs the processing actions.</span></span> <span data-ttu-id="fa184-160">قد تتضمن هذه الإجراءات تحويل مستندات الأعمال إلى فاتورة إلكترونية، وتطبيق توقيع إلكتروني، وإرسال المستند إلى خدمة ويب خارجية.</span><span class="sxs-lookup"><span data-stu-id="fa184-160">These actions might include transforming the business document into an electronic invoice, applying an electronic signature, and submitting the document to an external web service.</span></span>
4. <span data-ttu-id="fa184-161">ويتم تخزين كافة المستندات المستلمة والمعالجة في Azure Blob storage الخاص بالعميل.</span><span class="sxs-lookup"><span data-stu-id="fa184-161">All the received and processed documents are stored in the customer's Azure Blob storage.</span></span>
5. <span data-ttu-id="fa184-162">يتم تخزين كافة أسرار وشهادات المستأجر التي تم استخدامها للمعالجة في Azure Key Vault الخاص بالعميل.</span><span class="sxs-lookup"><span data-stu-id="fa184-162">All the tenant secrets and certificates that were used for processing are stored in the customer's Azure key vault.</span></span>
6. <span data-ttu-id="fa184-163">توفر الخدمة معلومات عند الطلب للعميل حول حالة معالجة مستند الأعمال الذي تم إرساله.</span><span class="sxs-lookup"><span data-stu-id="fa184-163">The service provides on-demand information to the client about the processing status of the business document that was sent.</span></span>
7. <span data-ttu-id="fa184-164">يتلقى العميل معلومات حول تنفيذ المعالجة المكتملة ويجعل كافة معلومات السجل متوفرة.</span><span class="sxs-lookup"><span data-stu-id="fa184-164">The client receives information about the completed processing execution and makes all the log information available.</span></span> <span data-ttu-id="fa184-165">ويجعل أيضًا المستند الذي تم إنشاؤه أو تلقيه أثناء معالجة سير المهام متوفرًا.</span><span class="sxs-lookup"><span data-stu-id="fa184-165">It also makes the document that was created or received during flow processing available.</span></span>

<span data-ttu-id="fa184-166">يبين الرسم التوضيحي التالي كيفية تدفق البيانات إلى ومن الوظيفة الإضافية الفوترة الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="fa184-166">The following illustration shows how data flows to and from the Electronic invoicing add-on.</span></span>

![تدفق البيانات للوظيفة الإضافية الفوترة الإلكترونية](media/e-invoicing-service-data-flow-diagram-overview.png)

## <a name="privacy-notice"></a><span data-ttu-id="fa184-168">إشعار الخصوصية</span><span class="sxs-lookup"><span data-stu-id="fa184-168">Privacy notice</span></span>
<span data-ttu-id="fa184-169">قد يتطلب تمكين واستخدام الفوترة الإلكترونية إرسال بيانات محدودة، تتضمن معرف التسجيل الضريبي للمؤسسة.</span><span class="sxs-lookup"><span data-stu-id="fa184-169">Enabling and using Electronic invoicing may require sending limited data, which includes the organization tax registration ID.</span></span> <span data-ttu-id="fa184-170">سيتم إرسال هذه البيانات إلى وكالات خارجية معتمدة من قبل هيئات الضرائب لأغراض إرسال الفواتير الإلكترونية إلى هيئة الضرائب هذه بالتنسيقات المعرفة مسبقًا والمطلوبة لإجراء التكامل مع خدمات الويب هذه الخاصة بالحكومة.</span><span class="sxs-lookup"><span data-stu-id="fa184-170">This will be transmitted to third-party agencies authorized by the tax authorities for purposes of sending electronic invoices in the predefined formats required for integration with these government’s web services.</span></span> <span data-ttu-id="fa184-171">تخضع البيانات المستوردة من هذه الأنظمة الخارجية في خدمة Dynamics 365 عبر الإنترنت [لبيان الخصوصية](https://go.microsoft.com/fwlink/?LinkId=512132).</span><span class="sxs-lookup"><span data-stu-id="fa184-171">Data imported from these external systems into this Dynamics 365 online service are subject to our [privacy statement](https://go.microsoft.com/fwlink/?LinkId=512132).</span></span> <span data-ttu-id="fa184-172">الرجاء مراجعه أقسام إشعار الخصوصية في وثائق الميزات الخاصة بالبلد لمزيد من المعلومات.</span><span class="sxs-lookup"><span data-stu-id="fa184-172">Consult the Privacy notice sections in country-specific feature documentation for more information.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="fa184-173">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="fa184-173">Additional resources</span></span>

- [<span data-ttu-id="fa184-174">بدء استخدام الوظيفة الإضافية "الفوترة الإلكترونية"</span><span class="sxs-lookup"><span data-stu-id="fa184-174">Get started with the Electronic invoicing add-on</span></span>](e-invoicing-get-started.md)
- [<span data-ttu-id="fa184-175">بدء استخدام الوظيفة الإضافية الفوترة الإلكترونية في البرازيل</span><span class="sxs-lookup"><span data-stu-id="fa184-175">Get started with the Electronic invoicing add-on for Brazil</span></span>](e-invoicing-bra-get-started.md)
- [<span data-ttu-id="fa184-176">بدء استخدام الوظيفة الإضافية الفوترة الإلكترونية في المكسيك</span><span class="sxs-lookup"><span data-stu-id="fa184-176">Get started with the Electronic invoicing add-on for Mexico</span></span>](e-invoicing-mex-get-started.md)
- [<span data-ttu-id="fa184-177">بدء استخدام الوظيفة الإضافية الفوترة الإلكترونية في إيطاليا</span><span class="sxs-lookup"><span data-stu-id="fa184-177">Get started with the Electronic invoicing add-on for Italy</span></span>](e-invoicing-ita-get-started.md)
- [<span data-ttu-id="fa184-178">إعداد الوظيفة الإضافية الفوترة الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="fa184-178">Set up the Electronic invoicing add-on</span></span>](e-invoicing-setup.md)