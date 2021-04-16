---
title: نظرة عامة على الفوترة الإلكترونية
description: يوفر هذا الموضوع معلومات حول الفوترة الإلكترونية في Microsoft Dynamics 365 Finance وفي Dynamics 365 Supply Chain Management.
author: gionoder
ms.date: 03/29/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: a6a8ea3fcad980dc02f489e07a7b21fe1c1b5a5a
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/01/2021
ms.locfileid: "5839970"
---
# <a name="electronic-invoicing-overview"></a><span data-ttu-id="36658-103">نظرة عامة على الفوترة الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="36658-103">Electronic invoicing overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="36658-104">تُعد الفوترة الإلكترونية لكل من Microsoft Dynamics 365 Finance وDynamics 365 Supply Chain Management خدمة متعددة المستأجرين قابلة للتوسعة بشكل كبير. وهي تمكّن المعالجة القابلة للتكوين لمستندات الفواتير الإلكترونية ومبادلة المستندات القابلة للتكوين.</span><span class="sxs-lookup"><span data-stu-id="36658-104">Electronic invoicing for Microsoft Dynamics 365 Finance and Dynamics 365 Supply Chain Management is a hyper-scalable multitenant service that enables configurable processing of electronic invoice documents and configurable document exchange.</span></span> <span data-ttu-id="36658-105">قواعد المعالجة والتكامل قابلة للتكوين بشكل كامل، ويتم تشغيل المنطق خارج Finance وSupply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="36658-105">The processing and integration rules are fully configurable, and the logic is run outside Finance and Supply Chain Management.</span></span> <span data-ttu-id="36658-106">تستهدف الخدمة بشكل أساسي معالجة الفواتير الإلكترونية في سيناريوهات الأعمال إلى الحكومة، ولكن يمكن تكوينها بشكل مخصص لأغراض أخرى.</span><span class="sxs-lookup"><span data-stu-id="36658-106">The service is targeted mainly at e-invoice processing in business-to-government scenarios, but it can be custom-configured for other purposes.</span></span>

<span data-ttu-id="36658-107">بإمكان الفوترة الإلكترونية أن تساعدك على تحقيق الأهداف التالية:</span><span class="sxs-lookup"><span data-stu-id="36658-107">Electronic invoicing can help you achieve the following goals:</span></span>

- <span data-ttu-id="36658-108">اعتماد سريع وسهل للمتطلبات الخاصة بالبلدان/المناطق</span><span class="sxs-lookup"><span data-stu-id="36658-108">Fast and easy adoption of country/region-specific requirements</span></span>
- <span data-ttu-id="36658-109">عمليات تنفيذ موحدة لحل الفوترة الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="36658-109">Standardized implementations of an Electronic invoicing solution</span></span>
- <span data-ttu-id="36658-110">إمكانية تتبع محسنة لمحفوظات المستندات</span><span class="sxs-lookup"><span data-stu-id="36658-110">Enhanced traceability of document history</span></span>
- <span data-ttu-id="36658-111">دورة تنفيذ أقصر</span><span class="sxs-lookup"><span data-stu-id="36658-111">Shorter implementation cycle</span></span>
- <span data-ttu-id="36658-112">إجمالي تكلفة ملكية منخفضة (TCO)</span><span class="sxs-lookup"><span data-stu-id="36658-112">Reduced total cost of ownership (TCO)</span></span>
- <span data-ttu-id="36658-113">تكوينات سهله التعديل لا تتطلب تغييرات في التعليمات البرمجية</span><span class="sxs-lookup"><span data-stu-id="36658-113">Easily adjustable configurations that don't required code changes</span></span>
- <span data-ttu-id="36658-114">إنشاء حزم تكوين بشكل مبسّط</span><span class="sxs-lookup"><span data-stu-id="36658-114">Simplified configuration packaging</span></span>
- <span data-ttu-id="36658-115">عمليات تصدير واستيراد وتكامل مضمنة، وقابلية توسعة سهلة في معالجة مستندات الفواتير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="36658-115">Built-in export, import, and integration, and easy extensibility in the processing of e-invoice documents</span></span>
- <span data-ttu-id="36658-116">سهولة إعادة استخدام تكوينات التصدير والاستيراد والتكامل عبر الشركات.</span><span class="sxs-lookup"><span data-stu-id="36658-116">Easy reuse of the same export, import, and integration configurations across companies</span></span>

<span data-ttu-id="36658-117">لاستخدام الفوترة الإلكتروني، يجب تثبيتها من المشروع في Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="36658-117">To use Electronic invoicing, you must install it from your project in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="36658-118">بعد ذلك، اتبع إجراء الإعداد لتشغيل التكامل مع Finance أو Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="36658-118">Next, follow the setup procedure to turn on the integration with Finance or Supply Chain Management.</span></span> <span data-ttu-id="36658-119">لمزيد من المعلومات، راجع [بدء استخدام الفوترة الإلكترونية](e-invoicing-get-started.md).</span><span class="sxs-lookup"><span data-stu-id="36658-119">For more information, see [Get started with Electronic invoicing](e-invoicing-get-started.md).</span></span>

## <a name="service-availability"></a><span data-ttu-id="36658-120">توفر خدمة <a name="availability"></a></span><span class="sxs-lookup"><span data-stu-id="36658-120"><a name="availability"></a>Service availability</span></span>

<span data-ttu-id="36658-121">تتوفر الفوترة الإلكترونية حاليًا للعملاء من خلال برنامج المعاينة، وفي المرحلة التالية، ستكون الخدمة متوفرة بشكل عام.</span><span class="sxs-lookup"><span data-stu-id="36658-121">Currently Electronic invoicing is available to customers through the preview program, and in the next phase, the service will become generally available.</span></span> <span data-ttu-id="36658-122">لأن الوظيفة التي تقوم بمعالجة المتطلبات الخاصة بالبلدان/المناطق قد تكون محدودة في مراحل مختلفة من الإصدار، يجب عليك دائمًا التحقق من الوثائق الحديثة التي تلقي الضوء على تغطية ونطاق الحلول الخاصة بالبلدان/المناطق.</span><span class="sxs-lookup"><span data-stu-id="36658-122">Because functionality that addresses country/region-specific requirements might be limited at different phases of the release, you should always check the most up-to-date documentation that highlights the coverage and scope of supported country/region-specific solutions.</span></span>

<span data-ttu-id="36658-123">يتم نشر الفوترة الإلكترونية في مناطق Azure الجغرافية التالية:</span><span class="sxs-lookup"><span data-stu-id="36658-123">Electronic invoicing is deployed in the following Azure geographies:</span></span>

- <span data-ttu-id="36658-124">الولايات المتحدة</span><span class="sxs-lookup"><span data-stu-id="36658-124">United States</span></span>
- <span data-ttu-id="36658-125">أوروبا</span><span class="sxs-lookup"><span data-stu-id="36658-125">Europe</span></span>

> [!NOTE]
> <span data-ttu-id="36658-126">لا تدعم الفوترة الإلكترونية عمليات النشر المحلية.</span><span class="sxs-lookup"><span data-stu-id="36658-126">Electronic invoicing doesn't support on-premises deployments.</span></span>

## <a name="extended-configurability"></a><span data-ttu-id="36658-127">قابلية تكوين موسعة</span><span class="sxs-lookup"><span data-stu-id="36658-127">Extended configurability</span></span>

<span data-ttu-id="36658-128">يمكن استخدام الفوترة الإلكترونية في السيناريوهات حيث يجب عليك إنشاء مستند الكتروني وإرساله إلى الأطراف المعينة.</span><span class="sxs-lookup"><span data-stu-id="36658-128">Electronic invoicing can be used in scenarios where you must create and send an electronic document to the designated parties.</span></span> <span data-ttu-id="36658-129">لقد تم تصميمها خصيصًا لتشغيل سير مهام قابل للتكوين من إجراءات المعالجة، استنادًا إلى البيانات المستلمة.</span><span class="sxs-lookup"><span data-stu-id="36658-129">It's specifically designed for running a configurable flow of processing actions, based on received data.</span></span> <span data-ttu-id="36658-130">تقتصر خيارات قابلية التكوين المتوفرة في Finance وSupply Chain Management على تحويل المستندات.</span><span class="sxs-lookup"><span data-stu-id="36658-130">The configurability options that are available in Finance and Supply Chain Management are limited to document transformation.</span></span> <span data-ttu-id="36658-131">تقوم الخدمة بتوسيع هذه الخيارات عن طريق إضافة عمليات تكامل قابلة للتكوين متوفرة فيها.</span><span class="sxs-lookup"><span data-stu-id="36658-131">The service extends these options by adding the configurable integrations that are available in it.</span></span> <span data-ttu-id="36658-132">علاوةً على ذلك، فإن جميع وظائف الفواتير الإلكترونية التي كانت متوفرة في وقت سابق، مثل Brazilian Nota fiscal eletrônica (NF-e) أو Mexican Comprobante Fiscal Digital por Internet (CFDI) أو لغة الأعمال العامة (UBL) لأوروبا الشرقية/Pan-European Public Procurement OnLine (PEPPOL)، ستستخدم تكوينات التصدير والاستيراد، ولتمكين التكامل مع خدمات الويب الخارجية.</span><span class="sxs-lookup"><span data-stu-id="36658-132">In addition, all the electronic invoice functionalities that were previously available, such as Brazilian Nota fiscal eletrônica (NF-e), Mexican Comprobante Fiscal Digital por Internet (CFDI), or other Western European Universal Business Language (UBL)/Pan-European Public Procurement OnLine (PEPPOL) functionalities, will use configurations for export and import, and to enable integrations with external web services.</span></span>

## <a name="feature-highlights"></a><span data-ttu-id="36658-133">النقاط الرئيسية في الميزات</span><span class="sxs-lookup"><span data-stu-id="36658-133">Feature highlights</span></span>

- <span data-ttu-id="36658-134">تكامل جاهز مع Finance وSupply Chain Management</span><span class="sxs-lookup"><span data-stu-id="36658-134">Out-of-box integration with Finance and Supply Chain management</span></span>
- <span data-ttu-id="36658-135">تجربة مستخدم متسقة لتكوين ومراقبة عملية الفاتورة الإلكترونية لجميع البلدان أو المناطق</span><span class="sxs-lookup"><span data-stu-id="36658-135">Consistent user experience for the configuration and monitoring of the e-invoice process for all countries or regions</span></span>
- <span data-ttu-id="36658-136">اعتماد أسهل وأسرع وأقل تكلفة لحلول الفوترة الإلكترونية في بلدان أو مناطق جديدة</span><span class="sxs-lookup"><span data-stu-id="36658-136">Faster, easier, and less expensive adoption of Electronic invoicing solutions in new countries or regions</span></span>
- <span data-ttu-id="36658-137">تكوين الخدمة من خلال Regulatory Configuration Services (RCS) وإعداد ميزة العولمة.</span><span class="sxs-lookup"><span data-stu-id="36658-137">Configuration of the service through the Regulatory Configuration Service (RCS) and Globalization feature setup</span></span>
- <span data-ttu-id="36658-138">تحويل بيانات العمل إلى تنسيقات الفواتير الإلكترونية المتعددة (XML وJavaScript Object Notation \[JSON\] وTXT والقيم المفصولة بفواصل \[CSV\]) باستخدام التكوينات المعرّفة في RCS:</span><span class="sxs-lookup"><span data-stu-id="36658-138">Transformation of business data into multiple e-invoice formats (XML, JavaScript Object Notation \[JSON\], TXT, and comma-separated values \[CSV\]) by using configurations that are defined in RCS:</span></span>

    - <span data-ttu-id="36658-139">تنسيقات التقارير الإلكترونية المتاحة للبلدان أو المناطق التي لا تتوفر فيها عملية تحويل الفاتورة الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="36658-139">Electronic reporting formats that are available for countries or regions where configurability for e-invoice transformation isn't available</span></span>

- <span data-ttu-id="36658-140">الإرسال القابل للتكوين للفواتير الإلكترونية إلى خدمات الويب الخارجية، بما في ذلك معالجة الشهادة من خلال التوقيعات الرقمية:</span><span class="sxs-lookup"><span data-stu-id="36658-140">Configurable submission of e-invoices to external web services, including certification handling through digital signatures:</span></span>

    - <span data-ttu-id="36658-141">تكامل مدمج وسهل التوسعة وقابل للتكوين مع محتوى إضافي لبلدان متعددة</span><span class="sxs-lookup"><span data-stu-id="36658-141">Built-in, easily extendable, and configurable integration with additional content for several countries</span></span>

    > [!NOTE]
    > <span data-ttu-id="36658-142">في الوقت الحالي، هناك عدد محدود مدعوم من عمليات الإرسال المباشرة.</span><span class="sxs-lookup"><span data-stu-id="36658-142">Currently, a limited number of direct submissions are supported.</span></span> <span data-ttu-id="36658-143">لمزيد من المعلومات، راجع القسم [توفر الخدمة](#availability) سالف الذكر في هذا الموضوع.</span><span class="sxs-lookup"><span data-stu-id="36658-143">For more information, see the [Service availability](#availability) section earlier in this topic.</span></span> <span data-ttu-id="36658-144">سيتم تقديم الدعم في المستقبل.</span><span class="sxs-lookup"><span data-stu-id="36658-144">Support will be extended in the future.</span></span>

- <span data-ttu-id="36658-145">معالجة الاستجابات من خدمات الويب، بما في ذلك معالجة رسالة الاستثناء القابلة للتكوين</span><span class="sxs-lookup"><span data-stu-id="36658-145">Handling of responses from web services, including configurable exception message handling</span></span>
- <span data-ttu-id="36658-146">دعم التوقيعات الإلكترونية (على سبيل المثال، باستخدام خوارزمية التوقيع XMLDSig)</span><span class="sxs-lookup"><span data-stu-id="36658-146">Support for electronic signatures (for example, by using the XMLDSig signing algorithm)</span></span>
- <span data-ttu-id="36658-147">المعالجة الدُفعية لرسائل الفاتورة الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="36658-147">Batch processing of e-invoice messages</span></span>

## <a name="architecture-and-data-flow"></a><span data-ttu-id="36658-148">البنية وتدفق البيانات</span><span class="sxs-lookup"><span data-stu-id="36658-148">Architecture and data flow</span></span>

<span data-ttu-id="36658-149">عندما يتم تثبيت الفوترة الإلكترونية من LCS، وتم إكمال الإعداد المطلوب في كافة التطبيقات المطلوبة، يتم تأسيس اتصال آمن.</span><span class="sxs-lookup"><span data-stu-id="36658-149">When Electronic invoicing is installed from LCS, and the required setup is completed in all required applications, a secure connection is established.</span></span> <span data-ttu-id="36658-150">توجد الخدمة حاليًا في مراكز البيانات في الولايات المتحدة وأوروبا.</span><span class="sxs-lookup"><span data-stu-id="36658-150">The service is currently located in data centers in the United States and Europe.</span></span> <span data-ttu-id="36658-151">وبالتالي، قد يختلف موقع الخدمة عن موقع مثيل Finance أو Supply Chain Management المرتبط.</span><span class="sxs-lookup"><span data-stu-id="36658-151">Therefore, the service location might differ from the location of the related Finance or Supply Chain Management instance.</span></span> <span data-ttu-id="36658-152">بعد إكمال إعداد الفوترة الإلكترونية وتشغيل التكامل، وكلما تم إرسال فاتورة إلكترونية، يتم إرسال البيانات الرئيسية وبيانات المعاملات المرتبطة بمستند معين إلى الفوترة الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="36658-152">After you complete the setup of Electronic invoicing and turn on the integration, whenever an electronic invoice is sent, master data and transactional data that are related to a specific document are sent to Electronic invoicing.</span></span>

> [!NOTE]
> <span data-ttu-id="36658-153">إذا احتوت فاتورتك الإلكترونية أو أي مستند آخر على بيانات شخصية، تأكد من أن استخدامك لهذه الميزة يلبي القانون العام لحماية البيانات (GDPR) واللوائح الأخرى المرتبطة بنقل البيانات الشخصية.</span><span class="sxs-lookup"><span data-stu-id="36658-153">If your electronic invoice or any other document contains personal data, verify that your use of this feature meets the General Data Protection Regulation (GDPR) and other regulations that are related to the transfer of personal data.</span></span>

### <a name="high-level-description-of-the-data-flow"></a><span data-ttu-id="36658-154">وصف عالي المستوي لتدفق البيانات</span><span class="sxs-lookup"><span data-stu-id="36658-154">High-level description of the data flow</span></span>

1. <span data-ttu-id="36658-155">يقوم العميل بإرسال مستند أعمال متعارف عليه إلى الخدمة.</span><span class="sxs-lookup"><span data-stu-id="36658-155">The client sends a canonical business document to the service.</span></span>
2. <span data-ttu-id="36658-156">استنادًا إلى معلومات السياق التي يتم تلقيها من العميل، تحدد الخدمة سير مهام المعالجة القابل للتطبيق.</span><span class="sxs-lookup"><span data-stu-id="36658-156">Based on the context information that is received from the client, the service selects the applicable processing flow.</span></span>
3. <span data-ttu-id="36658-157">تعمل الخدمة على تشغيل إجراءات المعالجة.</span><span class="sxs-lookup"><span data-stu-id="36658-157">The service runs the processing actions.</span></span> <span data-ttu-id="36658-158">قد تتضمن هذه الإجراءات تحويل مستندات الأعمال إلى فاتورة إلكترونية، وتطبيق توقيع إلكتروني، وإرسال المستند إلى خدمة ويب خارجية.</span><span class="sxs-lookup"><span data-stu-id="36658-158">These actions might include transforming the business document into an electronic invoice, applying an electronic signature, and submitting the document to an external web service.</span></span>
4. <span data-ttu-id="36658-159">ويتم تخزين كافة المستندات المستلمة والمعالجة في Azure Blob storage الخاص بالعميل.</span><span class="sxs-lookup"><span data-stu-id="36658-159">All the received and processed documents are stored in the customer's Azure Blob storage.</span></span>
5. <span data-ttu-id="36658-160">يتم تخزين كافة أسرار وشهادات المستأجر التي تم استخدامها للمعالجة في Azure Key Vault الخاص بالعميل.</span><span class="sxs-lookup"><span data-stu-id="36658-160">All the tenant secrets and certificates that were used for processing are stored in the customer's Azure key vault.</span></span>
6. <span data-ttu-id="36658-161">توفر الخدمة معلومات عند الطلب للعميل حول حالة معالجة مستند الأعمال الذي تم إرساله.</span><span class="sxs-lookup"><span data-stu-id="36658-161">The service provides on-demand information to the client about the processing status of the business document that was sent.</span></span>
7. <span data-ttu-id="36658-162">يتلقى العميل معلومات حول تنفيذ المعالجة المكتملة ويجعل كافة معلومات السجل متوفرة.</span><span class="sxs-lookup"><span data-stu-id="36658-162">The client receives information about the completed processing execution and makes all the log information available.</span></span> <span data-ttu-id="36658-163">ويجعل أيضًا المستند الذي تم إنشاؤه أو تلقيه أثناء معالجة سير المهام متوفرًا.</span><span class="sxs-lookup"><span data-stu-id="36658-163">It also makes the document that was created or received during flow processing available.</span></span>

<span data-ttu-id="36658-164">يبين الرسم التوضيحي التالي كيفية تدفق البيانات إلى ومن الفوترة الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="36658-164">The following illustration shows how data flows to and from Electronic invoicing.</span></span>

![تدفق البيانات للفوترة الإلكترونية](media/e-invoicing-service-data-flow-diagram-overview.png)

## <a name="privacy-notice"></a><span data-ttu-id="36658-166">إشعار الخصوصية</span><span class="sxs-lookup"><span data-stu-id="36658-166">Privacy notice</span></span>
<span data-ttu-id="36658-167">قد يتطلب تمكين واستخدام الفوترة الإلكترونية إرسال بيانات محدودة، تتضمن معرف التسجيل الضريبي للمؤسسة.</span><span class="sxs-lookup"><span data-stu-id="36658-167">Enabling and using Electronic invoicing may require sending limited data, which includes the organization tax registration ID.</span></span> <span data-ttu-id="36658-168">سيتم إرسال هذه البيانات إلى وكالات خارجية معتمدة من قبل هيئات الضرائب لأغراض إرسال الفواتير الإلكترونية إلى هيئة الضرائب هذه بالتنسيقات المعرفة مسبقًا والمطلوبة لإجراء التكامل مع خدمات الويب هذه الخاصة بالحكومة.</span><span class="sxs-lookup"><span data-stu-id="36658-168">This will be transmitted to third-party agencies authorized by the tax authorities for purposes of sending electronic invoices in the predefined formats required for integration with these government’s web services.</span></span> <span data-ttu-id="36658-169">تخضع البيانات المستوردة من هذه الأنظمة الخارجية في خدمة Dynamics 365 عبر الإنترنت [لبيان الخصوصية](https://go.microsoft.com/fwlink/?LinkId=512132).</span><span class="sxs-lookup"><span data-stu-id="36658-169">Data imported from these external systems into this Dynamics 365 online service are subject to our [privacy statement](https://go.microsoft.com/fwlink/?LinkId=512132).</span></span> <span data-ttu-id="36658-170">الرجاء مراجعه أقسام إشعار الخصوصية في وثائق الميزات الخاصة بالبلد لمزيد من المعلومات.</span><span class="sxs-lookup"><span data-stu-id="36658-170">Consult the Privacy notice sections in country-specific feature documentation for more information.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="36658-171">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="36658-171">Additional resources</span></span>
- [<span data-ttu-id="36658-172">إدارة الخدمة</span><span class="sxs-lookup"><span data-stu-id="36658-172">Service administration</span></span>](e-invoicing-service-administration.md)
- [<span data-ttu-id="36658-173">تكوين الفواتير الإلكترونية في RCS</span><span class="sxs-lookup"><span data-stu-id="36658-173">Configure electronic invoices in RCS</span></span>](e-invoicing-configuration-rcs.md)
- [<span data-ttu-id="36658-174">إصدار الفواتير الإلكترونية في Finance وفي Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="36658-174">Issue electronic invoices in Finance and Supply Chain Management</span></span>](e-invoicing-issuing-electronic-invoices-finance-supply-chain-management.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
