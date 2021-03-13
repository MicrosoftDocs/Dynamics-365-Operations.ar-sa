---
title: نوع وجهة إعداد التقارير الإلكترونية للأرشيف
description: يوفر هذا الموضوع معلومات حول كيفيه تكوين وجهه أرشفه لكل مجلد أو مكون ملف لتنسيق التقارير الكترونيه (ER).
author: NickSelin
manager: AnnBe
ms.date: 11/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: DocuType, ERSolutionTable, ERFormatDestinationTable
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 0067024d7a29e2a1db3b7fdba9ea3c6a63aad648
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/30/2021
ms.locfileid: "5094119"
---
# <a name="archive-er-destination-type"></a><span data-ttu-id="b1011-103">نوع وجهة إعداد التقارير الإلكترونية للأرشيف</span><span class="sxs-lookup"><span data-stu-id="b1011-103">Archive ER destination type</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b1011-104">يمكنك تكوين وجهة أرشيف لكل مكون **مجلد** أو **ملف** لتنسيق إعداد التقارير الإلكترونية (ER) التي يتم تكوينها لإنشاء مستندات صادرة.</span><span class="sxs-lookup"><span data-stu-id="b1011-104">You can configure an archive destination for each **Folder** or **File** component of an Electronic reporting (ER) format that is configured to generate outbound documents.</span></span> <span data-ttu-id="b1011-105">واستنادًا إلى إعداد الوجهة، يتم تخزين المستند المنشأ كمرفق لسجل قائمة مهام إعداد التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="b1011-105">Based on the destination setting, a generated document is stored as an attachment of a record of the ER jobs list.</span></span> <span data-ttu-id="b1011-106">لعرض النتائج، انتقل إلى **إدارة مؤسسة** \> **التقارير الإلكترونية** \> **وظائف إعداد التقارير الإلكترونية**.</span><span class="sxs-lookup"><span data-stu-id="b1011-106">To view the results, go to **Organization administration** \> **Electronic reporting** \> **Electronic reporting jobs**.</span></span>

<span data-ttu-id="b1011-107">يمكنك استخدام هذا الخيار لإرسال المستند المنشأ إلى مجلد Microsoft SharePoint أو مساحة تخزين Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="b1011-107">You can use this option to send the generated document to a Microsoft SharePoint folder or Microsoft Azure Storage.</span></span> <span data-ttu-id="b1011-108">عيّن الخيار **ممكّن** إلى **نعم** لإرسال المخرجات إلى وجهة تم تعريفها بواسطة نوع المستند المحدد.</span><span class="sxs-lookup"><span data-stu-id="b1011-108">Set **Enabled** to **Yes** to send output to a destination that is defined by the selected document type.</span></span> <span data-ttu-id="b1011-109">أنواع المستندات المتوفرة للتحديد هي فقط تلك التي تم تعيين المجموعة فيها إلى **ملف**.</span><span class="sxs-lookup"><span data-stu-id="b1011-109">Only document types where the group is set to **File** are available for selection.</span></span> <span data-ttu-id="b1011-110">يمكنك تحديد [أنواع](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-document-management#configure-document-types) المستندات في **إدارة المؤسسة** \> **إدارة المستند** \> **أنواع المستندات**.</span><span class="sxs-lookup"><span data-stu-id="b1011-110">You define document [types](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-document-management#configure-document-types) at **Organization administration** \> **Document management** \> **Document types**.</span></span> <span data-ttu-id="b1011-111">يُعد تكوين وجهات التقارير الإلكتروني التكوين نفسه لنظام إدارة المستندات.</span><span class="sxs-lookup"><span data-stu-id="b1011-111">The configuration for ER destinations is the same as the configuration for the document management system.</span></span>

<span data-ttu-id="b1011-112">[![صفحة أنواع المستندات](./media/ER_Destinations-SharePointDocuType.png)](./media/ER_Destinations-SharePointDocuType.png)</span><span class="sxs-lookup"><span data-stu-id="b1011-112">[![Document types page](./media/ER_Destinations-SharePointDocuType.png)](./media/ER_Destinations-SharePointDocuType.png)</span></span>

<span data-ttu-id="b1011-113">يحدد الموقع المكان حيث تم حفظ الملف.</span><span class="sxs-lookup"><span data-stu-id="b1011-113">The location determines where the file is saved.</span></span> <span data-ttu-id="b1011-114">بعد تمكين وجهة **الأرشيف**، يمكن حفظ النتائج تنفيذ التكوين في أرشيف الوظيفة.</span><span class="sxs-lookup"><span data-stu-id="b1011-114">After the **Archive** destination is enabled, the results can be saved in the Job archive.</span></span> <span data-ttu-id="b1011-115">يمكنك عرض النتائج في **إدارة مؤسسة** \> **التقارير الإلكترونية** \> **الوظائف المؤرشفة لإعداد التقارير الإلكترونية**.</span><span class="sxs-lookup"><span data-stu-id="b1011-115">You can view the results at **Organization administration** \> **Electronic reporting** \> **Electronic reporting archived jobs**.</span></span>

> [!NOTE]
> <span data-ttu-id="b1011-116">حدد نوع مستند لأرشيف الوظيفة بالتنقل إلى **إدارة المؤسسة** \> **مساحات العمل** \> **التقارير الإلكترونية** \> **معلمات التقارير الإلكترونية**.</span><span class="sxs-lookup"><span data-stu-id="b1011-116">Select a document type for the Job archive by navigating to **Organization administration** \> **Workspaces** \> **Electronic reporting** \> **Electronic reporting parameters**.</span></span> <span data-ttu-id="b1011-117">للحصول على مزيد من التفاصيل، راجع [تكوين إطار عمل إعداد التقارير الإلكترونية (ER)](electronic-reporting-er-configure-parameters.md#prerequisites-for-er-setup).</span><span class="sxs-lookup"><span data-stu-id="b1011-117">For more information, see [Configure the Electronic reporting (ER) framework](electronic-reporting-er-configure-parameters.md#prerequisites-for-er-setup).</span></span>

## <a name="sharepoint"></a><span data-ttu-id="b1011-118">SharePoint</span><span class="sxs-lookup"><span data-stu-id="b1011-118">SharePoint</span></span>

<span data-ttu-id="b1011-119">يمكنك حفظ ملف في مجلد معين في SharePoint.</span><span class="sxs-lookup"><span data-stu-id="b1011-119">You can save a file in a designated SharePoint folder.</span></span> <span data-ttu-id="b1011-120">لتحديد خادم SharePoint الافتراضي، انتقل إلى **إدارة المؤسسة** \> **إدارة المستندات** \> **معلمات إدارة المستندات**.</span><span class="sxs-lookup"><span data-stu-id="b1011-120">To define the default SharePoint server, go to **Organization administration** \> **Document management** \> **Document management parameters**.</span></span> <span data-ttu-id="b1011-121">في علامة التبويب **SharePoint**، كوِّن مجلد SharePoint.</span><span class="sxs-lookup"><span data-stu-id="b1011-121">On the **SharePoint** tab, configure the SharePoint folder.</span></span> <span data-ttu-id="b1011-122">يمكنك بعد ذلك تحديده كمجلد حفظ مخرجات التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="b1011-122">Then, you can select it as the folder where the ER output will be saved.</span></span> <span data-ttu-id="b1011-123">يجب تحديد موقع **SharePoint** في نوع المستند هذا.</span><span class="sxs-lookup"><span data-stu-id="b1011-123">The **SharePoint** location must be selected in this document type.</span></span>

<span data-ttu-id="b1011-124">[![تحديد مجلد SharePoint](./media/ER_Destinations-SharePointDocuTypeLocation.png)](./media/ER_Destinations-SharePointDocuTypeLocation.png)</span><span class="sxs-lookup"><span data-stu-id="b1011-124">[![Selecting a SharePoint folder](./media/ER_Destinations-SharePointDocuTypeLocation.png)](./media/ER_Destinations-SharePointDocuTypeLocation.png)</span></span>

## <a name="azure-storage"></a><span data-ttu-id="b1011-125">Azure Storage</span><span class="sxs-lookup"><span data-stu-id="b1011-125">Azure Storage</span></span>

<span data-ttu-id="b1011-126">عند تعيين موقع نوع المستند إلى **مساحة تخزين Azure**، يمكنك حفظ ملف في مساحة تخزين Azure.</span><span class="sxs-lookup"><span data-stu-id="b1011-126">When the document type location is set to **Azure storage**, you can save a file to Azure Storage.</span></span>

> [!NOTE] 
> <span data-ttu-id="b1011-127">يقوم إطار عمل إعداد التقارير الإلكترونية بتخزين الملفات بشكل دائم في تخزين Azure Blob بخلاف إطار عمل إدارة البيانات الذي يطبق نهج الاحتفاظ لمدة سبعة أيام للمستندات التي يجب معالجتها.</span><span class="sxs-lookup"><span data-stu-id="b1011-127">The ER framework permanently stores files in Azure Blob storage unlike the Data management framework that applies the seven-day retention policy for documents that must be processed.</span></span> <span data-ttu-id="b1011-128">لمزيد من المعلومات، راجع [واجهة برمجة التطبيقات للحصول على حالة الرسالة](../data-entities/recurring-integrations.md#api-for-getting-message-status) و[واجهة برمجة تطبيقات التحقق من الحالة](../data-entities/data-management-api.md#status-check-api).</span><span class="sxs-lookup"><span data-stu-id="b1011-128">For more information, see [API for getting message status](../data-entities/recurring-integrations.md#api-for-getting-message-status) and [Status check API](../data-entities/data-management-api.md#status-check-api).</span></span> <span data-ttu-id="b1011-129">سيتم تخزين الملفات المتعلقة بالتقارير الإلكترونية في تخزين Azure Blob كمرفقات في سجلات جدول التطبيق طالما كان ذلك ضروريًا.</span><span class="sxs-lookup"><span data-stu-id="b1011-129">The ER-related files will be stored in Azure Blob storage as attachments of application table records as long as necessary.</span></span> <span data-ttu-id="b1011-130">سيتم حذف ملف واحد من تخزين Azure Blob مع سجل جدول التطبيق الذي تم إرفاق هذا الملف به.</span><span class="sxs-lookup"><span data-stu-id="b1011-130">A single file will be deleted from Azure Blob storage along with the application table record that this file was attached to.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b1011-131">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="b1011-131">Additional resources</span></span>

- [<span data-ttu-id="b1011-132">نظرة عامة على إعداد التقارير الإلكترونية (ER)</span><span class="sxs-lookup"><span data-stu-id="b1011-132">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="b1011-133">وجهات إعداد التقارير الإلكترونية (ER)‬</span><span class="sxs-lookup"><span data-stu-id="b1011-133">Electronic reporting (ER) destinations</span></span>](electronic-reporting-destinations.md)
- [<span data-ttu-id="b1011-134">تكوين إدارة المستندات</span><span class="sxs-lookup"><span data-stu-id="b1011-134">Configure document management</span></span>](../../fin-ops/organization-administration/configure-document-management.md)
