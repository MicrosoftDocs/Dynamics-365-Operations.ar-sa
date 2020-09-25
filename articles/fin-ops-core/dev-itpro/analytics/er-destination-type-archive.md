---
title: نوع وجهة إعداد التقارير الإلكترونية للأرشيف
description: يوفر هذا الموضوع معلومات حول كيفية تكوين وجهة أرشيف لكل مكون "ملف" أو "مجلد" لتنسيق إعداد التقارير الإلكترونية (ER) التي يتم تكوينها لإنشاء مستندات صادرة.
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
ms.openlocfilehash: 8797a68507a5116c6adbf1f2d805838fa507958c
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745575"
---
# <a name="archive-destination"></a><span data-ttu-id="b828f-103">وجهة الأرشيف</span><span class="sxs-lookup"><span data-stu-id="b828f-103">Archive destination</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b828f-104">يمكنك تكوين وجهة أرشيف لكل مكون "ملف" أو "مجلد" لتنسيق إعداد التقارير الإلكترونية (ER) التي يتم تكوينها لإنشاء مستندات صادرة.</span><span class="sxs-lookup"><span data-stu-id="b828f-104">You can configure an archive destination for each FOLDER or FILE component of an Electronic reporting (ER) format that is configured to generate outbound documents.</span></span> <span data-ttu-id="b828f-105">واستنادًا إلى إعداد الوجهة، يتم تخزين المستند المنشأ كمرفق لسجل قائمة مهام إعداد التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="b828f-105">Based on the destination setting, a generated document is stored as an attachment of a record of the ER jobs list.</span></span>

<span data-ttu-id="b828f-106">يمكنك استخدام هذا الخيار لإرسال المستند المنشأ إلى مجلد Microsoft SharePoint أو مساحة تخزين Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="b828f-106">You can use this option to send the generated document to a Microsoft SharePoint folder or Microsoft Azure Storage.</span></span> <span data-ttu-id="b828f-107">عيّن الخيار **ممكّن** إلى **نعم**لإرسال المخرجات إلى وجهة تم تعريفها بواسطة نوع المستند المحدد.</span><span class="sxs-lookup"><span data-stu-id="b828f-107">Set **Enabled** to **Yes** to send output to a destination that is defined by the selected document type.</span></span> <span data-ttu-id="b828f-108">أنواع المستندات المتوفرة للتحديد هي فقط تلك التي تم تعيين المجموعة فيها إلى **ملف**.</span><span class="sxs-lookup"><span data-stu-id="b828f-108">Only document types where the group is set to **File** are available for selection.</span></span> <span data-ttu-id="b828f-109">يمكنك تحديد [أنواع](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-document-management#configure-document-types) المستندات في **إدارة المؤسسة** \> **إدارة المستند** \> **أنواع المستندات**.</span><span class="sxs-lookup"><span data-stu-id="b828f-109">You define document [types](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-document-management#configure-document-types) at **Organization administration** \> **Document management** \> **Document types**.</span></span> <span data-ttu-id="b828f-110">يُعد تكوين وجهات التقارير الإلكتروني التكوين نفسه لنظام إدارة المستندات.</span><span class="sxs-lookup"><span data-stu-id="b828f-110">The configuration for ER destinations is the same as the configuration for the document management system.</span></span>

<span data-ttu-id="b828f-111">[![صفحة أنواع المستندات](./media/ER_Destinations-SharePointDocuType.png)](./media/ER_Destinations-SharePointDocuType.png)</span><span class="sxs-lookup"><span data-stu-id="b828f-111">[![Document types page](./media/ER_Destinations-SharePointDocuType.png)](./media/ER_Destinations-SharePointDocuType.png)</span></span>

<span data-ttu-id="b828f-112">يحدد الموقع المكان حيث تم حفظ الملف.</span><span class="sxs-lookup"><span data-stu-id="b828f-112">The location determines where the file is saved.</span></span> <span data-ttu-id="b828f-113">بعد تمكين وجهة **الأرشيف**، يمكن حفظ النتائج تنفيذ التكوين في أرشيف الوظيفة.</span><span class="sxs-lookup"><span data-stu-id="b828f-113">After the **Archive** destination is enabled, the results can be saved in the Job archive.</span></span> <span data-ttu-id="b828f-114">يمكنك عرض النتائج في **إدارة مؤسسة** \> **التقارير الإلكترونية** \> **الوظائف المؤرشفة لإعداد التقارير الإلكترونية**.</span><span class="sxs-lookup"><span data-stu-id="b828f-114">You can view the results at **Organization administration** \> **Electronic reporting** \> **Electronic reporting archived jobs**.</span></span>

> [!NOTE]
> <span data-ttu-id="b828f-115">حدد نوع مستند لأرشيف الوظيفة بالتنقل إلى **إدارة المؤسسة** \> **مساحات العمل** \> **التقارير الإلكترونية** \> **معلمات التقارير الإلكترونية**.</span><span class="sxs-lookup"><span data-stu-id="b828f-115">Select a document type for the Job archive by navigating to **Organization administration** \> **Workspaces** \> **Electronic reporting** \> **Electronic reporting parameters**.</span></span> <span data-ttu-id="b828f-116">للحصول على مزيد من التفاصيل، [تكوين إطار عمل إعداد التقارير الإلكترونية (ER)](electronic-reporting-er-configure-parameters.md#prerequisites-for-er-setup).</span><span class="sxs-lookup"><span data-stu-id="b828f-116">For more information, [Configure the Electronic reporting (ER) framework](electronic-reporting-er-configure-parameters.md#prerequisites-for-er-setup).</span></span>

## <a name="sharepoint"></a><span data-ttu-id="b828f-117">SharePoint</span><span class="sxs-lookup"><span data-stu-id="b828f-117">SharePoint</span></span>

<span data-ttu-id="b828f-118">يمكنك حفظ ملف في مجلد معين في SharePoint.</span><span class="sxs-lookup"><span data-stu-id="b828f-118">You can save a file in a designated SharePoint folder.</span></span> <span data-ttu-id="b828f-119">لتحديد خادم SharePoint الافتراضي، انتقل إلى **إدارة المؤسسة** \> **إدارة المستندات** \> **معلمات إدارة المستندات**.</span><span class="sxs-lookup"><span data-stu-id="b828f-119">To define the default SharePoint server, go to **Organization administration** \> **Document management** \> **Document management parameters**.</span></span> <span data-ttu-id="b828f-120">في علامة التبويب **SharePoint**، كوِّن مجلد SharePoint.</span><span class="sxs-lookup"><span data-stu-id="b828f-120">On the **SharePoint** tab, configure the SharePoint folder.</span></span> <span data-ttu-id="b828f-121">يمكنك بعد ذلك تحديده كمجلد حفظ مخرجات التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="b828f-121">Then, you can select it as the folder where the ER output will be saved.</span></span> <span data-ttu-id="b828f-122">يجب تحديد موقع **SharePoint** في نوع المستند هذا.</span><span class="sxs-lookup"><span data-stu-id="b828f-122">The **SharePoint** location must be selected in this document type.</span></span>

<span data-ttu-id="b828f-123">[![تحديد مجلد SharePoint](./media/ER_Destinations-SharePointDocuTypeLocation.png)](./media/ER_Destinations-SharePointDocuTypeLocation.png)</span><span class="sxs-lookup"><span data-stu-id="b828f-123">[![Selecting a SharePoint folder](./media/ER_Destinations-SharePointDocuTypeLocation.png)](./media/ER_Destinations-SharePointDocuTypeLocation.png)</span></span>

## <a name="azure-storage"></a><span data-ttu-id="b828f-124">Azure Storage</span><span class="sxs-lookup"><span data-stu-id="b828f-124">Azure Storage</span></span>

<span data-ttu-id="b828f-125">عند تعيين موقع نوع المستند إلى **مساحة تخزين Azure**، يمكنك حفظ ملف في مساحة تخزين Azure.</span><span class="sxs-lookup"><span data-stu-id="b828f-125">When the document type location is set to **Azure storage**, you can save a file to Azure Storage.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b828f-126">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="b828f-126">Additional resources</span></span>

- [<span data-ttu-id="b828f-127">نظرة عامة على إعداد التقارير الإلكترونية (ER)</span><span class="sxs-lookup"><span data-stu-id="b828f-127">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="b828f-128">وجهات إعداد التقارير الإلكترونية (ER)‬</span><span class="sxs-lookup"><span data-stu-id="b828f-128">Electronic reporting (ER) destinations</span></span>](electronic-reporting-destinations.md)
- [<span data-ttu-id="b828f-129">تكوين إدارة المستندات</span><span class="sxs-lookup"><span data-stu-id="b828f-129">Configure document management</span></span>](../../fin-ops/organization-administration/configure-document-management.md)
