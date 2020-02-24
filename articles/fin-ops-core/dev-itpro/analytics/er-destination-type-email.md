---
title: نوع البريد الإلكتروني لوجهة إعداد التقارير الإلكترونية
description: يوفر هذا الموضوع معلومات حول كيفية تكوين وجهة بريد إلكتروني لكل مكون "ملف" أو "مجلد" لتنسيق إعداد التقارير الإلكترونية (ER) التي يتم تكوينها لإنشاء مستندات صادرة.
author: NickSelin
manager: AnnBe
ms.date: 01/27/2020
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
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 086114d6a8d425ca01521d9607e4a70ec5aa766b
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/04/2020
ms.locfileid: "3019606"
---
# <span data-ttu-id="27ae0-103"><a name="EmailDestinationType">وجهة البريد الإلكتروني</a></span><span class="sxs-lookup"><span data-stu-id="27ae0-103"><a name="EmailDestinationType">Email destination</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="27ae0-104">يمكنك تكوين وجهة بريد إلكتروني لكل مكون "ملف" أو "مجلد" لتنسيق إعداد التقارير الإلكترونية (ER) التي يتم تكوينها لإنشاء مستندات صادرة.</span><span class="sxs-lookup"><span data-stu-id="27ae0-104">You can configure an email destination for each FOLDER or FILE component of an Electronic reporting (ER) format that is configured to generate outbound documents.</span></span> <span data-ttu-id="27ae0-105">واستنادًا إلى إعداد الوجهة، يتم تسليم المستند المنشأ كمرفق لبريد إلكتروني.</span><span class="sxs-lookup"><span data-stu-id="27ae0-105">Based on the destination setting, a generated document is delivered as an attachment of an electronic mail.</span></span>

<span data-ttu-id="27ae0-106">عيّن الخيار **ممكّن**إلى **نعم** لإرسال ملف المخرجات بواسطة البريد الإلكتروني.</span><span class="sxs-lookup"><span data-stu-id="27ae0-106">Set **Enabled** to **Yes** to send an output file by email.</span></span> <span data-ttu-id="27ae0-107">وبعد تمكين هذا الخيار، يمكنك تحديد مستلمي البريد الإلكتروني وتحرير الموضوع ونص رسالة البريد الإلكتروني.</span><span class="sxs-lookup"><span data-stu-id="27ae0-107">After this option is enabled, you can specify the email recipients and edit the subject and body of the email message.</span></span> <span data-ttu-id="27ae0-108">يمكنك إعداد نصوص ثابتة لموضوع البريد الإلكتروني والنص، أو يمكنك استخدام [معادلات](er-formula-language.md) إعداد التقارير الإلكترونية لإنشاء نصوص البريد الإلكتروني بطريقة ديناميكية.</span><span class="sxs-lookup"><span data-stu-id="27ae0-108">You can set up constant texts for the email subject and body, or you can use ER [formulas](er-formula-language.md) to dynamically create email texts.</span></span> 

<span data-ttu-id="27ae0-109">يمكنك تكوين عناوين البريد الإلكتروني للتقارير الإلكترونية بطريقتين.</span><span class="sxs-lookup"><span data-stu-id="27ae0-109">You can configure email addresses for ER in two ways.</span></span> <span data-ttu-id="27ae0-110">يمكن إكمال التكوين بنفس طريقة إكمال ميزة إدارة الطباعة لها، أو يمكنك حل عنوان بريد إلكتروني باستخدام مرجع مباشر لتكوين إعداد التقارير الإلكترونية من خلال إحدى المعادلات.</span><span class="sxs-lookup"><span data-stu-id="27ae0-110">The configuration can be completed in the same way that the Print management feature completes it, or you can resolve an email address by using a direct reference to the ER configuration through a formula.</span></span>

<span data-ttu-id="27ae0-111">[![تمكين وجهة البريد الإلكتروني](./media/ER_Destinations-EnableSingleDestination.png)](./media/ER_Destinations-EnableSingleDestination.png)</span><span class="sxs-lookup"><span data-stu-id="27ae0-111">[![Enable email destination](./media/ER_Destinations-EnableSingleDestination.png)](./media/ER_Destinations-EnableSingleDestination.png)</span></span>

## <a name="email-address-types"></a><span data-ttu-id="27ae0-112">أنواع عناوين البريد الإلكتروني</span><span class="sxs-lookup"><span data-stu-id="27ae0-112">Email address types</span></span>

<span data-ttu-id="27ae0-113">عند تحديد **تحرير** في الحقول **إلى** أو **نسخة**، يظهر مربع الحوار **بريد إلكتروني إلى**.</span><span class="sxs-lookup"><span data-stu-id="27ae0-113">When you select **Edit** in the **To** or **Cc** fields, the **Email to** dialog box appears.</span></span> <span data-ttu-id="27ae0-114">ثم يمكنك تحديد نوع عنوان البريد الإلكتروني المُراد استخدامه.</span><span class="sxs-lookup"><span data-stu-id="27ae0-114">You can then select the type of email address to use.</span></span> <span data-ttu-id="27ae0-115">يحظى حاليًا نوعا البريد الإلكتروني **البريد الإلكتروني للتكوين** و**إدارة الطباعة** بالدعم.</span><span class="sxs-lookup"><span data-stu-id="27ae0-115">The **Configuration email** and **Print Management** email types are currently supported.</span></span>

<span data-ttu-id="27ae0-116">[![تحديد نوع البريد الإلكتروني](./media/ER_Destinations-EmailSelectAddressType.png)](./media/ER_Destinations-EmailSelectAddressType.png)</span><span class="sxs-lookup"><span data-stu-id="27ae0-116">[![Select email type](./media/ER_Destinations-EmailSelectAddressType.png)](./media/ER_Destinations-EmailSelectAddressType.png)</span></span>

### <a name="print-management"></a><span data-ttu-id="27ae0-117">إدارة الطباعة</span><span class="sxs-lookup"><span data-stu-id="27ae0-117">Print management</span></span>

<span data-ttu-id="27ae0-118">عند تحديد نوع البريد الإلكتروني **إدارة الطباعة"**، يمكنك إدخال عناوين بريد إلكتروني ثابتة في حقل **إلى**.</span><span class="sxs-lookup"><span data-stu-id="27ae0-118">If you select the **Print Management** email type, you can enter fixed email addresses in the **To** field.</span></span> 

<span data-ttu-id="27ae0-119">[![تكوين عناوين البريد الكتروني الثابتة](./media/ER_Destinations-EmailFixedAddress.png)](./media/ER_Destinations-EmailFixedAddress.png)</span><span class="sxs-lookup"><span data-stu-id="27ae0-119">[![Configure fixed email addresses](./media/ER_Destinations-EmailFixedAddress.png)](./media/ER_Destinations-EmailFixedAddress.png)</span></span>

<span data-ttu-id="27ae0-120">لاستخدام عناوين بريد إلكتروني غير ثابتة، يجب تحديد نوع مصدر البريد الإلكتروني لوجهة ملف.</span><span class="sxs-lookup"><span data-stu-id="27ae0-120">To use email addresses that aren't fixed, you must select the email source type for a file destination.</span></span> <span data-ttu-id="27ae0-121">القيم التالية مدعومة: **العميل**، **المورد**، **عميل متوقع**، **جهة اتصال**، **المنافس**، **العامل**، **مقدم الطلب**، **المورد المتوقع**، و **مورد غير مسموح به**.</span><span class="sxs-lookup"><span data-stu-id="27ae0-121">The following values are supported: **Customer**, **Vendor**, **Prospect**, **Contact**, **Competitor**, **Worker**, **Applicant**, **Prospective vendor**, and **Disallowed vendor**.</span></span> <span data-ttu-id="27ae0-122">بعد تحديد نوع مصدر البريد إلكتروني، استخدم الزر الموجود بجوار حقل **حساب مصدر البريد الإلكتروني** لفتح نموذج **مصمم المعادلة**.</span><span class="sxs-lookup"><span data-stu-id="27ae0-122">After you select an email source type, use the button next to the **Email source account** field to open the **Formula designer** form.</span></span> <span data-ttu-id="27ae0-123">يمكنك استخدام هذا النموذج لإرفاق معادلة إرجاع في وقت التشغيل **، حساب الطرف** لنوع المصدر المحدد من المستند الذي تمت معالجته إلى وجهة البريد الإلكتروني.</span><span class="sxs-lookup"><span data-stu-id="27ae0-123">You can use this form to attach a formula that returns at runtime, the **party account** of the selected source type from the processed document to the email destination.</span></span>

<span data-ttu-id="27ae0-124">[![تكوين حساب مصدر البريد الإلكتروني](./media/ER_Destinations-EmailDefineAddressSource.png)](./media/ER_Destinations-EmailDefineAddressSource.png)</span><span class="sxs-lookup"><span data-stu-id="27ae0-124">[![Configure email source account](./media/ER_Destinations-EmailDefineAddressSource.png)](./media/ER_Destinations-EmailDefineAddressSource.png)</span></span>

<span data-ttu-id="27ae0-125">تتعلق المعادلات بتكوين إعداد التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="27ae0-125">Formulas are specific to the ER configuration.</span></span> <span data-ttu-id="27ae0-126">في حقل **المعادلة** أدخل مرجعًا خاصًا بالمستند إلى طرف من نوع عميل أو مورّد.</span><span class="sxs-lookup"><span data-stu-id="27ae0-126">In the **Formula** field, enter a document-specific reference to a customer or vendor party type.</span></span> <span data-ttu-id="27ae0-127">بدلاً من الكتابة، يمكنك العثور على عقدة مصدر البيانات التي تمثل حساب العميل أو المورّد، ثم حدد الزر **إضافة مصدر البيانات** لتحديث المعادلة.</span><span class="sxs-lookup"><span data-stu-id="27ae0-127">Instead of typing, you can find the data source node that represents the customer or vendor account, and then select **Add data source** to update the formula.</span></span> <span data-ttu-id="27ae0-128">على سبيل المثال، إذا كنت تستخدم تكوين **نقل الائتمان ISO 20022**، فإن العقدة التي تمثل حساب المورّد هي `'\$PaymentsForCoveringLetter'.Creditor.Identification.SourceID`.</span><span class="sxs-lookup"><span data-stu-id="27ae0-128">For example, if you use the **ISO 20022 Credit Transfer** configuration, the node that represents a vendor account is `'\$PaymentsForCoveringLetter'.Creditor.Identification.SourceID`.</span></span>

<span data-ttu-id="27ae0-129">عند إدخال قيمة سلسلة، مثل `"DE-001"`، وحفظ إحدى المعادلات، سيتم إرسال بريد إلكتروني إلى شخص جهة الاتصال بالمورد، **DE-001**.</span><span class="sxs-lookup"><span data-stu-id="27ae0-129">If you enter a string value, such as `"DE-001"`, and save a formula, an email will be sent to the contact person of the vendor, **DE-001**.</span></span>


<span data-ttu-id="27ae0-130">[![صفحة مصمم معادلة إعداد التقارير الإلكترونية](./media/ER_Destinations-EmailDefineAddressSourceFormula.png)](./media/ER_Destinations-EmailDefineAddressSourceFormula.png)</span><span class="sxs-lookup"><span data-stu-id="27ae0-130">[![ER formula designer page](./media/ER_Destinations-EmailDefineAddressSourceFormula.png)](./media/ER_Destinations-EmailDefineAddressSourceFormula.png)</span></span>

<span data-ttu-id="27ae0-131">[![تكوين حساب مصدر البريد الإلكتروني](./media/ER_Destinations-EmailDefineAddressSourceAttributes.png)](./media/ER_Destinations-EmailDefineAddressSourceAttributes.png)</span><span class="sxs-lookup"><span data-stu-id="27ae0-131">[![Configure email source account](./media/ER_Destinations-EmailDefineAddressSourceAttributes.png)](./media/ER_Destinations-EmailDefineAddressSourceAttributes.png)</span></span>



### <a name="configuration-email"></a><span data-ttu-id="27ae0-132">البريد الإلكتروني في التكوين</span><span class="sxs-lookup"><span data-stu-id="27ae0-132">Configuration email</span></span>

<span data-ttu-id="27ae0-133">استخدم هذا النوع من البريد الإلكتروني إذا كان التكوين الذي تستخدمه به عقدة في مصادر البيانات التي ترجع **عنوان بريد إلكتروني**.</span><span class="sxs-lookup"><span data-stu-id="27ae0-133">Use this email type if the configuration that you use has a node in the data sources that returns an **email address**.</span></span> <span data-ttu-id="27ae0-134">يمكنك استخدام مصادر البيانات والوظائف في مصمم المعادلة للحصول على عنوان بريد إلكتروني منسق بشكل صحيح.</span><span class="sxs-lookup"><span data-stu-id="27ae0-134">You can use data sources and functions in the formula designer to get a correctly formatted email address.</span></span> <span data-ttu-id="27ae0-135">على سبيل المثال، إذا كنت تستخدم تكوين **نقل الائتمان ISO 20022**، فإن العقدة التي تمثل عنوان البريد الإلكتروني لشخص جهة الاتصال بالمورد هي `'$PaymentsForCoveringLetter'.Creditor.ContactDetails.Email`.</span><span class="sxs-lookup"><span data-stu-id="27ae0-135">For example, if you use the **ISO 20022 Credit Transfer** configuration, the node that represents an email address of a vendor's contact person is `'$PaymentsForCoveringLetter'.Creditor.ContactDetails.Email`.</span></span>

<span data-ttu-id="27ae0-136">[![تكوين مصدر عنوان البريد الإلكتروني](./media/ER_Destinations-EmailDefineAddressSource2.png)](./media/ER_Destinations-EmailDefineAddressSource2.png)</span><span class="sxs-lookup"><span data-stu-id="27ae0-136">[![Configure email address source](./media/ER_Destinations-EmailDefineAddressSource2.png)](./media/ER_Destinations-EmailDefineAddressSource2.png)</span></span>

## <a name="additional-resources"></a><span data-ttu-id="27ae0-137">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="27ae0-137">Additional resources</span></span>

- [<span data-ttu-id="27ae0-138">نظرة عامة على إعداد التقارير الإلكترونية (ER)</span><span class="sxs-lookup"><span data-stu-id="27ae0-138">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="27ae0-139">وجهات إعداد التقارير الإلكترونية (ER)‬</span><span class="sxs-lookup"><span data-stu-id="27ae0-139">Electronic reporting (ER) destinations</span></span>](electronic-reporting-destinations.md)
- [<span data-ttu-id="27ae0-140">مصمم المعادلات في التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="27ae0-140">Formula designer in Electronic reporting (ER)</span></span>](general-electronic-reporting-formula-designer.md)
