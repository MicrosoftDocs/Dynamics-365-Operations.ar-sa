---
title: الاستيراد المتقدم للتسوية البنكية MT940 - ترقية كيان بيانات مركب
description: يجب إضافة رقم تسلسلي إلى كيان استيراد كشف الحساب البنكي لدعم تنسيق MT940.
author: panolte
manager: AnnBe
ms.date: 06/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 221594
ms.assetid: dddc99ae-56ae-48df-856a-131079c17dcb
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 65970cdac114b72363d2fbbc08766c99ace00b88
ms.sourcegitcommit: 74b10104338222a945684d841d60ab4b8e570168
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/28/2020
ms.locfileid: "3899363"
---
# <a name="advanced-bank-reconciliation-mt940-import--composite-data-entity-upgrade"></a><span data-ttu-id="82d08-103">الاستيراد المتقدم للتسوية البنكية MT940 - ترقية كيان بيانات مركب</span><span class="sxs-lookup"><span data-stu-id="82d08-103">Advanced bank reconciliation MT940 Import – Composite data entity upgrade</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="82d08-104">يجب إضافة رقم تسلسلي إلى كيان استيراد كشف الحساب البنكي لدعم تنسيق MT940.</span><span class="sxs-lookup"><span data-stu-id="82d08-104">A sequence number needs to be added to the bank statement import entity to support the MT940 format.</span></span> 

<span data-ttu-id="82d08-105">استخدم الخطوات التالية لإضافة كيان استيراد كشف الحساب البنكي لدعم التنسيق MT940.</span><span class="sxs-lookup"><span data-stu-id="82d08-105">Use the following steps to add the bank statement import entity to support the MT940 format.</span></span>

1.  <span data-ttu-id="82d08-106">تجميع ومزامنة ما يلي:</span><span class="sxs-lookup"><span data-stu-id="82d08-106">Compile and synchronize the following:</span></span>
    -   <span data-ttu-id="82d08-107">الكيان المركب\\BankStatementImportEntity</span><span class="sxs-lookup"><span data-stu-id="82d08-107">Composite Entity\\BankStatementImportEntity</span></span>
    -   <span data-ttu-id="82d08-108">الكيان\\BankStatementBalanceEntity</span><span class="sxs-lookup"><span data-stu-id="82d08-108">Entity\\BankStatementBalanceEntity</span></span>
    -   <span data-ttu-id="82d08-109">الكيان\\BankStatementDocumentEntity</span><span class="sxs-lookup"><span data-stu-id="82d08-109">Entity\\BankStatementDocumentEntity</span></span>
    -   <span data-ttu-id="82d08-110">الكيان\\BankStatementEntity</span><span class="sxs-lookup"><span data-stu-id="82d08-110">Entity\\BankStatementEntity</span></span>
    -   <span data-ttu-id="82d08-111">الكيان\\BankStatementLineEntity</span><span class="sxs-lookup"><span data-stu-id="82d08-111">Entity\\BankStatementLineEntity</span></span>
    -   <span data-ttu-id="82d08-112">الجداول\\BankStatementStaging</span><span class="sxs-lookup"><span data-stu-id="82d08-112">Tables\\BankStatementStaging</span></span>

2.  <span data-ttu-id="82d08-113">إدارة البيانات\\مشاريع البيانات.</span><span class="sxs-lookup"><span data-stu-id="82d08-113">Data management\\data projects.</span></span>
    1.  <span data-ttu-id="82d08-114">تحميل مشروع (مشاريع) استيراد MT940</span><span class="sxs-lookup"><span data-stu-id="82d08-114">Load MT940 import project(s)</span></span>
        1.  <span data-ttu-id="82d08-115">تغيير XSLT.</span><span class="sxs-lookup"><span data-stu-id="82d08-115">Change XSLT.</span></span>
            -   <span data-ttu-id="82d08-116">انقر فوق **عرض الخريط**.</span><span class="sxs-lookup"><span data-stu-id="82d08-116">Click **View map**.</span></span>
            -   <span data-ttu-id="82d08-117">انقر فوق **عرض الخريطة** على مستند كشف الحساب البنكي.</span><span class="sxs-lookup"><span data-stu-id="82d08-117">Click **View map** on the bank statement document.</span></span>
            -   <span data-ttu-id="82d08-118">انقر فوق **التحويلات**</span><span class="sxs-lookup"><span data-stu-id="82d08-118">Click **Transformations**</span></span>
            -   <span data-ttu-id="82d08-119">احذف الملف BankReconiliation-to-Composite.xslt.</span><span class="sxs-lookup"><span data-stu-id="82d08-119">Delete the BankReconiliation-to-Composite.xslt file.</span></span>
            -   <span data-ttu-id="82d08-120">أضف إصدار BankReconiliation-to-Composite.xsl الجديد.</span><span class="sxs-lookup"><span data-stu-id="82d08-120">Add the new version of BankReconiliation-to-Composite.xsl.</span></span>

        2.  <span data-ttu-id="82d08-121">عرض **الرقم التسلسلي‬** على تخطيط **بيانات المصدر‬**.</span><span class="sxs-lookup"><span data-stu-id="82d08-121">Expose the **Sequence Number** on **Source Data** layout.</span></span>
            1.  <span data-ttu-id="82d08-122">تنسيق بيانات المصدر = عنصر XML.</span><span class="sxs-lookup"><span data-stu-id="82d08-122">Source data format = XML-Element.</span></span>
            2.  <span data-ttu-id="82d08-123">اسم الكيان = كشوف الحسابات البنكية.</span><span class="sxs-lookup"><span data-stu-id="82d08-123">Entity name = Bank statements.</span></span>
            3.  <span data-ttu-id="82d08-124">تحميل ملف البيانات = إصدار SampleBankCompositeEntity.xml الجديد.</span><span class="sxs-lookup"><span data-stu-id="82d08-124">Upload data file = new version SampleBankCompositeEntity.xml.</span></span>
            4.  <span data-ttu-id="82d08-125">انقر فوق **نعم** للكتابة فوق الملف الموجود.</span><span class="sxs-lookup"><span data-stu-id="82d08-125">Click **Yes** to overwrite the existing file.</span></span>
            5.  <span data-ttu-id="82d08-126">انقر فوق **نعم** لإنشاء تعيين جديد.</span><span class="sxs-lookup"><span data-stu-id="82d08-126">Click **Yes** to generate a new mapping.</span></span>
            6.  <span data-ttu-id="82d08-127">تأكد من تعيين**SequenceNumber**.</span><span class="sxs-lookup"><span data-stu-id="82d08-127">Verify that S**equenceNumber** is mapped.</span></span>
                -   <span data-ttu-id="82d08-128">انقر فوق **عرض الخريطة** على كيان كشف الحساب.</span><span class="sxs-lookup"><span data-stu-id="82d08-128">Click **View Map** on the statement entity.</span></span>
                -   <span data-ttu-id="82d08-129">تأكد من تعيين **SequenceNumber** من المصدر إلى التشغيل المرحلي‬.</span><span class="sxs-lookup"><span data-stu-id="82d08-129">Verify that **SequenceNumber** is mapped from Source to Staging.</span></span>

3.  <span data-ttu-id="82d08-130">استيراد كشف الحساب الجديد.</span><span class="sxs-lookup"><span data-stu-id="82d08-130">Import the new statement.</span></span>




