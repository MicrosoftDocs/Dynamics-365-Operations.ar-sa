---
title: نوع وجهة إعداد التقارير الإلكترونية للطابعة
description: يوضح هذا الموضوع كيفية تكوين وجهة طابعة لكل مكون "ملف" أو "مجلد" لتنسيق إعداد التقارير الإلكترونية (ER) التي يتم تكوينها لإنشاء مستندات صادرة بتنسيق PDF أو تنسيق Microsoft Office (Excel\Word).
author: NickSelin
manager: AnnBe
ms.date: 01/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: DocuType, ERSolutionTable, ERFormatDestinationTable
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-04-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 58e067baa130458e3a8e788d978604f208140a03
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/04/2020
ms.locfileid: "3019607"
---
# <a name="PrinterDestinationType"></a><span data-ttu-id="e1d63-103">وجهة الطابعة</span><span class="sxs-lookup"><span data-stu-id="e1d63-103">Printer destination</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e1d63-104">يمكنك إرسال مستند مُنشأ مباشرة إلى طابعة الشبكة للطباعة المباشرة.</span><span class="sxs-lookup"><span data-stu-id="e1d63-104">You can send a generated document directly to a network printer for direct printing.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="e1d63-105">المتطلبات الأساسية</span><span class="sxs-lookup"><span data-stu-id="e1d63-105">Prerequisites</span></span>

<span data-ttu-id="e1d63-106">قبل البدء، يجب تثبيت وكيل توجيه المستند وتكوينه، ثم تسجيل طابعات الشبكة.</span><span class="sxs-lookup"><span data-stu-id="e1d63-106">Before you begin, you must install and configure the Document Routing Agent, and then register the network printers.</span></span> <span data-ttu-id="e1d63-107">لمزيد من المعلومات، راجع [تثبيت وكيل توجيه المستند لتمكين طباعة الشبكة](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/install-document-routing-agent)</span><span class="sxs-lookup"><span data-stu-id="e1d63-107">For more information, see [Install the Document Routing Agent to enable network printing](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/install-document-routing-agent).</span></span>

## <a name="make-the-printer-destination-available"></a><span data-ttu-id="e1d63-108">توفير وجهة الطابعة</span><span class="sxs-lookup"><span data-stu-id="e1d63-108">Make the Printer destination available</span></span>

<span data-ttu-id="e1d63-109">لتوفير وجهة **الطابعة** في مثيل Microsoft Dynamics 365 Finance الحالي، انتقل إلى مساحة عمل **إدارة الميزات**، وشغَّل الميزات التالية بالترتيب التالي:</span><span class="sxs-lookup"><span data-stu-id="e1d63-109">To make the **Printer** destination available in the current instance of Microsoft Dynamics 365 Finance, go to the **Feature management** workspace, and turn on the following features, in this order:</span></span>

1. <span data-ttu-id="e1d63-110">تحويل المستندات الصادرة للتقارير الإلكترونية من تنسيقات Microsoft Office إلى PDF</span><span class="sxs-lookup"><span data-stu-id="e1d63-110">Convert Electronic Reporting outbound documents from Microsoft Office formats to PDF</span></span>
2. <span data-ttu-id="e1d63-111">عامل توجيه المستندات كوجهة إعداد التقارير الإلكترونية للمستندات الصادرة</span><span class="sxs-lookup"><span data-stu-id="e1d63-111">Document Routing Agent as Electronic Reporting destination for outbound documents</span></span>

<span data-ttu-id="e1d63-112">[![تشغيل ميزة وجهة طابعة إعداد التقارير الإلكترونية في إدارة الميزات](./media/ER_Destinations-EnablePrinterDestinationFeature.png)](./media/ER_Destinations-EnablePrinterDestinationFeature.png)</span><span class="sxs-lookup"><span data-stu-id="e1d63-112">[![Turning on the ER printer destination feature in Feature management](./media/ER_Destinations-EnablePrinterDestinationFeature.png)](./media/ER_Destinations-EnablePrinterDestinationFeature.png)</span></span>

### <a name="applicability"></a><span data-ttu-id="e1d63-113">إمكانية التطبيق</span><span class="sxs-lookup"><span data-stu-id="e1d63-113">Applicability</span></span>

<span data-ttu-id="e1d63-114">لا يمكن تكوين وجهة **الطابعة** إلا لمكونات الملف المستخدمة لإنشاء مخرجات في تنسيق pdf القابل للطباعة (عناصر تنسيق ملف PDF أو دمج PDF) أو تنسيق Microsoft Office Excel/Word (ملف Excel).</span><span class="sxs-lookup"><span data-stu-id="e1d63-114">The **Printer** destination can be configured only for file components that are used to generate output in either printable PDF format (PDF Merger or PDF file format elements) or Microsoft Office Excel/Word format (Excel file).</span></span> <span data-ttu-id="e1d63-115">عند إنشاء مخرجات بتنسيق PDF، يتم إرسالها إلى طابعة.</span><span class="sxs-lookup"><span data-stu-id="e1d63-115">When output is generated in PDF format, it's sent to a printer.</span></span> <span data-ttu-id="e1d63-116">عند إنشاء المخرجات بتنسيق Microsoft Office، يتم تحويلها تلقائيًا إلى تنسيق PDF ثم إرسالها إلى طابعة.</span><span class="sxs-lookup"><span data-stu-id="e1d63-116">When output is generated in Microsoft Office format, it's automatically converted to PDF format and then sent to a printer.</span></span>

### <a name="limitations"></a><span data-ttu-id="e1d63-117">قيود</span><span class="sxs-lookup"><span data-stu-id="e1d63-117">Limitations</span></span>

<span data-ttu-id="e1d63-118">هذه الميزة هي ميزة معاينة وهي خاضعة لشروط الاستخدام الموضحة في [شروط الاستخدام الإضافية لمعاينات المستخدمة لمعاينات Microsoft Dynamics 365](https://go.microsoft.com/fwlink/?linkid=2105274).</span><span class="sxs-lookup"><span data-stu-id="e1d63-118">This feature is a preview feature and is subject to the terms of use that are described in [Supplemental Terms of Use for Microsoft Dynamics 365 Previews](https://go.microsoft.com/fwlink/?linkid=2105274).</span></span>

<span data-ttu-id="e1d63-119">لا يتم تطبيق وجهة **الطابعة** إلا لعمليات نشر المجموعة فقط.</span><span class="sxs-lookup"><span data-stu-id="e1d63-119">The **Printer** destination is implemented only for cloud deployments.</span></span>

### <a name="use-the-printer-destination"></a><span data-ttu-id="e1d63-120">استخدام وجهة الطابعة</span><span class="sxs-lookup"><span data-stu-id="e1d63-120">Use the Printer destination</span></span>

1. <span data-ttu-id="e1d63-121">عيِّن الخيار **ممكَّن** على **نعم** لإرسال مستند منشأ إلى طابعة.</span><span class="sxs-lookup"><span data-stu-id="e1d63-121">Set the **Enabled** option to **Yes** to send a generated document to a printer.</span></span>
2. <span data-ttu-id="e1d63-122">في الحقل **اسم الطابعة**، حدد طابعة الشبكة المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="e1d63-122">In the **Printer name** field, select the required network printer.</span></span>
3. <span data-ttu-id="e1d63-123">عيِّن الخيار **هل تريد الحفظ في أرشيف الطباعة؟** على **نعم** لتخزين المخرجات المنشأة في أرشيف الطباعة، بحيث يكون متوفرًا لمزيد من عمليات الطباعة.</span><span class="sxs-lookup"><span data-stu-id="e1d63-123">Set the **Save in print archive?** option to **Yes** to store the generated output in the print archive, so that it's available for further printing.</span></span> <span data-ttu-id="e1d63-124">للوصول إلى المخرجات المؤرشفة لاحقًا، انتقل إلى **إدارة المؤسسة**\>**‏‫الاستعلامات والتقارير‬**\>**أرشيف التقارير**.</span><span class="sxs-lookup"><span data-stu-id="e1d63-124">To access archived output later, go to **Organization administration** \> **Inquiries and reports** \> **Report archive**.</span></span>

<span data-ttu-id="e1d63-125">[![استخدام وجهة الطابعة](./media/ER_Destinations-PrinterDestination.png)](./media/ER_Destinations-PrinterDestination.png)</span><span class="sxs-lookup"><span data-stu-id="e1d63-125">[![Using the Printer destination](./media/ER_Destinations-PrinterDestination.png)](./media/ER_Destinations-PrinterDestination.png)</span></span>

> [!NOTE]
> <span data-ttu-id="e1d63-126">لا يلزم تشغيل خيار **لتحويل إلى PDF‬** عند تكوين وجهة **الطابعة**.</span><span class="sxs-lookup"><span data-stu-id="e1d63-126">The **Convert to PDF** option doesn't have to be turned on when you configure the **Printer** destination.</span></span> <span data-ttu-id="e1d63-127">سيتم التحويل إلى PDF لأغراض الطباعة حتى في حالة إيقاف تشغيل الخيار.</span><span class="sxs-lookup"><span data-stu-id="e1d63-127">The PDF conversion for printing purposes will occur even if the option is turned off.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e1d63-128">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="e1d63-128">Additional resources</span></span>

- [<span data-ttu-id="e1d63-129">نظرة عامة على إعداد التقارير الإلكترونية (ER)</span><span class="sxs-lookup"><span data-stu-id="e1d63-129">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="e1d63-130">وجهات إعداد التقارير الإلكترونية (ER)‬</span><span class="sxs-lookup"><span data-stu-id="e1d63-130">Electronic reporting (ER) destinations</span></span>](electronic-reporting-destinations.md)
